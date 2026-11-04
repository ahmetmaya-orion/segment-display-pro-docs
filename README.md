# segment-display-pro-docs
User manual for the Segment Display Blender Add-on.

## Development

```
pip install -r requirements.txt
mkdocs serve
```

## Documentation versioning with mike

Public manual labels are `vX.Y`: `v1.0` covers Pro 1.0.x. The docs repository's
exact source tags are `v1.0.1`, `v1.0.1-corr.1`, `v1.0.1-corr.2`, etc. All these
snapshots update the same public `v1.0` manual. Never move a tag. No matching
manual release is required for a code-only patch. Describe changed patch
behavior with notes such as "Pro v1.0.1 and later."

Prepare current documentation on brain-support, review it, and merge approved
source into main before tagging. An old-family correction must start from its
latest source snapshot, preserving earlier corrections, not newer-family main.

### Automated workflow

- main/brain-support pushes and PRs to main: build validation, no publication.
- Pushed `vX.Y.Z` source tag: publish `vX.Y`, promote latest unless latest is
  already a newer family.
- Pushed `vX.Y.Z-corr.N` tag: update that family without moving latest elsewhere.
- Manual run: exact source tag, matching family, explicit latest promotion,
  dry-run defaulting to true.

A dry run builds the complete website artifact without pushing gh-pages or
publishing Pages. The workflow rejects invalid tags, mismatches, corrections
promoting latest, backwards latest promotion, corrections to uninitialized
families, and source history that would discard a previously published snapshot.
Published version metadata records source tag and commit. Retain source ancestry
when integrating fixes: a squash/rebase that drops the recorded source ancestor
may be rejected and requires deliberate source-history reconciliation, not
bypassing the safety check.

GitHub concurrency serializes this workflow, but is not a FIFO release queue
and may replace pending runs. Do not push multiple release tags in a batch;
wait for each deployment to complete. Do not publish locally while Actions runs.

The pipeline maintains gh-pages without force pushing, uploads the full site,
and deploys with GitHub Pages Actions. No personal access token is required.
If saving gh-pages succeeds but Pages deployment fails, inspect the failed job
and use a reviewed manual rerun of the same source; do not create/move a tag just
to retry. The public site may lag the generated branch until deployment succeeds.

### One-time migration

1. Preserve existing source and generated output. Never delete gh-pages as setup.
2. Review the setup and manual content. The recovery popup text/screenshots need
   a separate content check; infrastructure setup does not certify them.
3. Merge the approved setup to main. Its pushes validate only after replacement.
4. In Settings > Pages, change Source to **GitHub Actions**. Keep gh-pages as
   mike's generated-version store. This setting change is a user action, not
   part of applying files locally.
5. Ensure the github-pages environment permits deployment from intended release
   and correction tags. GitHub environment rules can otherwise block publication.
6. Create an annotated stable docs source tag only after review. Preview locally
   before pushing it: a matching tag push immediately publishes.
7. If the source tag already exists remotely, do not move it. A manual dry run
   can use it only if it contains the intended migrated setup and source.
8. Initial manual run: stable source tag, target v1.0, promote_latest=true,
   dry_run=true. Repeat with dry_run=false only after reviewing the artifact.
9. Verify the public root, version selector, relative images, links, and search.

For a brand-new tag needing a remote dry run before publication, do not push it
with automatic tag publishing enabled. Either preview locally before the normal
push or arrange a separately reviewed temporary disable/re-enable of the
publishing workflow. Do not disable workflow runs automatically during setup.

Mike preserves existing flat root files while adding versioned folders and
replacing the root index with the latest redirect. Legacy unversioned deep
links may continue serving stale flat output. Cleaning those files, redirects,
old search, and sitemaps is separate reviewed migration work, not an automatic
cleanup. Never run `mkdocs gh-deploy --force` after switching to mike.

### Local preview

```bash
git fetch origin
mkdocs serve
```

For real multi-version preview, stop the live server, then:

```bash
mike deploy v1.0
mike serve
```

Without --push, mike still commits to local gh-pages. It is not a dry run;
use a disposable clone for isolated previews so experimental commits cannot
accidentally be pushed later. Existing other manuals must be present on the
local deployment branch to appear. Redeploy after edits; mike serve is not a
live Markdown builder. Never pull generated gh-pages into the source branch.

On Ahmet's Windows system, the confirmed executables are:

```powershell
$mike = "$env:APPDATA\Python\Python314\Scripts\mike.exe"
& $mike --version
py -3.14 -m mkdocs --version
```

Use `& $mike` instead of bare mike if the Scripts folder is not on PATH.
`python -m mike` does not work: mike has no package __main__ entry point.

### Example: first release source

After review/merge to main, provided the tag does not already exist:

```bash
git switch main
git pull --ff-only
git tag -a v1.0.1 -m "Documentation source for Pro v1.0.1"
git switch --detach v1.0.1
mike deploy v1.0
mike serve
```

After local preview and explicit publication approval:

```bash
git push origin refs/tags/v1.0.1
```

Fork can perform switch, pull, annotated-tag creation and tagged-source checkout.
Detached checkout opens a fixed snapshot, suitable for building. Create a branch
before editing. Git operations and all publication still require user approval.

### Example: corrections

Review/merge the corrected current-family source into main first:

```bash
git switch main
git pull --ff-only
git tag -a v1.0.1-corr.1 -m "First correction to v1.0.1 manual source"
```

After preview and approval, push only that tag. Repeat on a later corrected
commit with v1.0.1-corr.2. Neither creates a public patch manual. For a later
v1.0.3 source release, its correction sequence starts at v1.0.3-corr.1.

If main is now v1.1, start the old correction branch from its latest applicable
source tag (example: v1.0.1-corr.1), commit the reviewed correction and create
v1.0.1-corr.2 there. Carry applicable fixes forward separately.

### Example: new family

Tag reviewed main source as v1.1.0, preview, then approve pushing the tag. It
publishes v1.1 and promotes latest; v1.0 remains available. Do not publish
manually as well as through the Action for the same release.

### Materials

materials/ is a local Affinity/export workspace, not an origin asset library.
Preserve its ignore rule. Copy only website-ready exports into docs/assets/
and commit images with relative Markdown references. Release-specific folders
under docs/assets/ are optional, not required. Git tags preserve source image
history and published manuals retain their own built image files.
