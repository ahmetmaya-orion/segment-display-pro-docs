# Changelog (Documentation)

Notable changes to the SegDisp Pro user manual. This history covers documentation, screenshots and instructions, not changes to the add-on code. Entries are grouped into patch and minor documentation updates; routine editorial corrections are not logged separately.

## v1.0.1

Updated documentation for the SegDisp v1.0.1 release.

### Added

- A Pro **[Review & Recover](prefs_and_settings.md#review-recover)** walkthrough covering library reconnection, node-tree restoration, optional modifier recreation, uncertain targets, backups and recovery results.
- Instructions for the **[About](prefs_and_settings.md#about-panel)** panels, version information, manual update checks, download links and [N-panel update-notification preferences](prefs_and_settings.md#n-panel-update-notifications).
- A separate documentation changelog, alongside the [add-on changelog](changelog_addon.md).

### Improved

- Explained when [reinstalling the complete matching package and restarting Blender](troubleshooting.md#displays-appear-as-planes-asset-not-available) may restore displays without manual recovery.
- Clarified [unsaved-project and backup-failure behavior](prefs_and_settings.md#backup-recover-and-save), recovery across scenes, [recognition properties](troubleshooting.md#pro-recognition-properties-and-modifiers), and the [limits of restoring deleted settings or animation](troubleshooting.md#recovery-limits-and-lost-settings). Missing-modifier recreation is explicitly opt-in and uses defaults.
- Distinguished [Pro recovery](prefs_and_settings.md#review-recover) from Lite's simplified Re-link operation without presenting a Lite recovery walkthrough as part of the Pro manual.
- Distinguished [Blender 5.1.1 as the declared minimum](installation.md#requirements) from Blender 5.1.2 as the tested/recommended version, retaining the caveat that v1.0.1 has not been re-tested on 5.1.1.
- Clarified the [Simple number-input limit of 10,000,000](in_cat_numbers.md#simple-number-inputs) and the [five 0-999 Complex input groups](in_cat_numbers.md#complex-number-input), including how display length and decimal formatting affect their use.
- Expanded the [16-segment font descriptions](display.md#16-segment-fonts) and aligned instruction terminology with the interface.
- Clarified that [generated display meshes may be exported to game engines and other software](faq.md#sharing-exporting); the redistribution restriction concerns the supplied asset .blend file. [Render-farm compatibility and render-node activation requirements](faq.md#licensing-usage) are explicitly unconfirmed.
- Retained clear [warnings against modifying the shipped asset file](troubleshooting.md#asset-safety) and against [treating recovery as a guarantee that deleted data can be restored](troubleshooting.md#recovery-limits-and-lost-settings).

### Images

- Updated annotated [Clock](in_cat_time.md#clock), [license-activation, About, update-notification and recovery screenshots](prefs_and_settings.md).
- Updated [display/font examples and labelled image comparisons](display.md) to support the revised instructions.
- Embedded the matching screenshots in the ClickUp manual in place of image-placeholder text.

## v1.0.0 (Initial Release)

The initial user manual for Segment Display Pro.

### Included

- Installation, license activation/deactivation, updating and uninstalling guidance.
- Descriptions of Numbers, Alphanumeric and Time inputs, including Clock, Timer and Date.
- Display models, segment fonts, materials, alignment, spacing, sizing and separator controls.
- Viewport preview and overlay instructions, with annotated interface screenshots and display examples.
- Requirements, edition comparisons, licensing information, troubleshooting and frequently asked questions.
