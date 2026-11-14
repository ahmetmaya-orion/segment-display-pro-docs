# Changelog (Documentation)

Notable changes to the SegDisp Pro user manual. This history covers documentation, screenshots and instructions, not changes to the add-on code. Entries are grouped into patch and minor documentation updates; routine editorial corrections are not logged separately.

## v1.0.0 (Initial Release)

The initial user manual for Segment Display Pro.

### Included

- Installation, license activation/deactivation, updating and uninstalling guidance.
- Descriptions of Numbers, Alphanumeric and Time inputs, including Clock, Timer and Date.
- Display models, segment fonts, materials, alignment, spacing, sizing and separator controls.
- Viewport preview and overlay instructions, with annotated interface screenshots and display examples.
- Requirements, edition comparisons, licensing information, troubleshooting and frequently asked questions.

## v1.0.1

Updated documentation for the SegDisp v1.0.1 release.

### Added

- A Pro **Review & Recover** walkthrough covering library reconnection, node-tree restoration, optional modifier recreation, uncertain targets, backups and recovery results.
- Instructions for the **About** panels, version information, manual update checks, download links and N-panel update-notification preferences.
- A separate documentation changelog, alongside the add-on changelog.

### Improved

- Explained when reinstalling the complete matching package and restarting Blender may restore displays without manual recovery.
- Clarified unsaved-project and backup-failure behavior, recovery across scenes, recognition properties, and the limits of restoring deleted settings or animation. Missing-modifier recreation is explicitly opt-in and uses defaults.
- Distinguished Pro recovery from Lite's simplified Re-link operation without presenting a Lite recovery walkthrough as part of the Pro manual.
- Distinguished Blender 5.1.1 as the declared minimum from Blender 5.1.2 as the tested/recommended version, retaining the caveat that v1.0.1 has not been re-tested on 5.1.1.
- Clarified the Simple number-input limit of 10,000,000 and the five 0-999 Complex input groups, including how display length and decimal formatting affect their use.
- Expanded the 16-segment font descriptions and aligned instruction terminology with the interface.
- Clarified that generated display meshes may be exported to game engines and other software; the redistribution restriction concerns the supplied asset .blend file. Render-farm compatibility and render-node activation requirements are explicitly unconfirmed.
- Retained clear warnings against modifying the shipped asset file and against treating recovery as a guarantee that deleted data can be restored.

### Images

- Updated annotated Clock, license-activation, About, update-notification and recovery screenshots.
- Updated display/font examples and labelled image comparisons to support the revised instructions.
- Embedded the matching screenshots in the ClickUp manual in place of image-placeholder text.
