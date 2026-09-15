# segment-display-pro-docs
User manual for the Segment Display Blender Add-on.

## Development

```
pip install -r requirements.txt
mkdocs serve
```

## Versioning with mike (installed, disabled)

[mike](https://github.com/jimporter/mike) lets multiple doc versions (e.g. `v1.0`, `v2.0`) live side by side on the same GitHub Pages site, with a version dropdown in the nav bar. It is installed via `requirements.txt` but **disabled** until needed.

To enable:

1. Uncomment the `extra.version` block in `mkdocs.yml`.
2. Replace the deploy step in `.github/workflows/deploy.yml` with the commented-out mike steps (and add the git identity step). Do **not** run `mkdocs gh-deploy --force` anymore afterwards - it force-pushes a flat site and would wipe all versions.
3. The existing `gh-pages` branch holds a flat (non-mike) deploy. For a clean start, delete `gh-pages` on origin before the first `mike deploy`, or accept stale files at the branch root.

Local testing (commits to a local branch only, add `--push` to publish):

```
mike deploy v1.0 latest --update-aliases
mike set-default latest
mike serve
```
