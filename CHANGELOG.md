# Changelog (Documentation)

Notable changes to the SegDisp Pro user manual. This history covers documentation, screenshots and instructions, not changes to the add-on code. Entries are grouped into patch and minor documentation updates; routine editorial corrections are not logged separately.

## v1.0.1

Updated documentation for the SegDisp v1.0.1 release.

### Added

- A Pro **[Review & Recover](docs/prefs_and_settings.md)** walkthrough covering library reconnection, node-tree restoration, optional modifier recreation, uncertain targets, backups and recovery results.
- Instructions for the **[About](docs/prefs_and_settings.md)** panels, version information, manual update checks, download links and [N-panel update-notification preferences](docs/prefs_and_settings.md).
- A separate documentation changelog, alongside the [add-on changelog](docs/changelog_addon.md).

### Improved

- Explained when [reinstalling the complete matching package and restarting Blender](docs/troubleshooting.md) may restore displays without manual recovery.
- Clarified [unsaved-project and backup-failure behavior](docs/prefs_and_settings.md), recovery across scenes, [recognition properties](docs/troubleshooting.md), and the [limits of restoring deleted settings or animation](docs/troubleshooting.md). Missing-modifier recreation is explicitly opt-in and uses defaults.
- Distinguished [Pro recovery](docs/prefs_and_settings.md) from Lite's simplified Re-link operation without presenting a Lite recovery walkthrough as part of the Pro manual.
- Distinguished [Blender 5.1.1 as the declared minimum](docs/installation.md) from Blender 5.1.2 as the tested/recommended version, retaining the caveat that v1.0.1 has not been re-tested on 5.1.1.
- Clarified the [Simple number-input limit of 10,000,000](docs/in_cat_numbers.md) and the [five 0-999 Complex input groups](docs/in_cat_numbers.md), including how display length and decimal formatting affect their use.
- Expanded the [16-segment font descriptions](docs/display.md) and aligned instruction terminology with the interface.
- Clarified that [generated display meshes may be exported to game engines and other software](docs/faq.md); the redistribution restriction concerns the supplied asset .blend file. [Render-farm compatibility and render-node activation requirements](docs/faq.md) are explicitly unconfirmed.
- Retained clear [warnings against modifying the shipped asset file](docs/troubleshooting.md) and against [treating recovery as a guarantee that deleted data can be restored](docs/troubleshooting.md).

### Images

- Updated annotated [Clock](docs/in_cat_time.md), [license-activation, About, update-notification and recovery screenshots](docs/prefs_and_settings.md).
- Updated [display/font examples and labelled image comparisons](docs/display.md) to support the revised instructions.
- Embedded the matching screenshots in the ClickUp manual in place of image-placeholder text.

## v1.0.0 (Initial Release)

The initial user manual for Segment Display Pro.

### Included

- Installation, license activation/deactivation, updating and uninstalling guidance.
- Descriptions of Numbers, Alphanumeric and Time inputs, including Clock, Timer and Date.
- Display models, segment fonts, materials, alignment, spacing, sizing and separator controls.
- Viewport preview and overlay instructions, with annotated interface screenshots and display examples.
- Requirements, edition comparisons, licensing information, troubleshooting and frequently asked questions.
