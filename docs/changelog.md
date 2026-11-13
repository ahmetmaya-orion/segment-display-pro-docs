
All notable changes to Segment Display Pro are listed here, newest first.

## v1.0.1

**Released:** 2026/11/08 &nbsp;·&nbsp; **Requires:** Blender 5.1 (Minimum 5.1.1) &nbsp;·&nbsp; **Tested and recommended:** Blender 5.1.2

A patch release with an About section and manual update checks, a Pro-only Review & Recover workflow for asset problems, and clearer asset and version notices. This patch has not yet been re-tested on Blender 5.1.1.

### Added

- **About:** in Preferences and at the bottom of the N-panel, showing Add-on Version, Assets Version, Compatible Blender and developer credits. See [About Panel](prefs_and_settings.md#about-panel).
- **Check for Updates:** a manual check in About, alongside the existing startup check. **Open Downloads** opens the release page; installation stays manual. See [Add-on Update](prefs_and_settings.md#add-on-update).
- **Hide update notifications:** an option to hide the N-panel header update notice. Update information remains available in About and Preferences. The preference is saved in `addon_userpref.json` outside the add-on folder, so it survives normal updates; for now it stores only this preference.
- **Review & Recover (Pro):** in **Preferences > Asset Status**. Preview supported library reconnections and missing node-tree repairs, review uncertain cases and pick the right modifier, optionally recreate a missing modifier with default settings, back up an already saved project first, and repair toggle inputs stored as numbers while keeping their on/off values. See [Review & Recover](prefs_and_settings.md#review-recover).
- **Recognition properties:** `segdisp_*` custom properties on Pro objects help recovery recognize displays. See [Pro recognition properties](troubleshooting.md#pro-recognition-properties-and-modifiers).
- **Email Support:** a new button in Resources & Support that opens your default mail app. See [Resources & Support](prefs_and_settings.md#resources-support-panel).

### Improved

- **Review & Recover** replaces the visible **Re-link Asset** button in Pro. Library reconnections can affect displays across scenes, and results show which items were left unchanged and which settings could not be restored.
- **Add Segment Display** checks for a missing asset or a known asset/add-on version mismatch before adding a display.
- Clearer asset availability, version mismatch and restart-required notices. Unavailable asset versions show as **Unknown** instead of a misleading value.
- N-panel asset warnings include a shortcut to Preferences.
- **About** and **Viewport & Overlays** start collapsed in the N-panel.
- Resources & Support documentation links point to the versioned v1.0 manual.

### Update Notes

!!! warning "Before and after updating"
    - Install the new complete Pro ZIP over the existing add-on, then **restart Blender** before troubleshooting. Keep a project backup before running any repair. See [Updating the Add-on](installation.md#updating-the-add-on).
    - Recovery does not save over your open project or guarantee that deleted settings come back. Review the result, then save.
    - Blender may stop responding for a while during asset processing. Let it finish.
    - Local asset copies, objects from the other edition and source-linked modifiers are not repaired directly. Linking displays from another project is not a validated workflow.
    - **Do not modify** the `segdisp_type`, `segdisp_schema`, `segdisp_edition` or `segdisp_modifier` custom properties.
    - License seat limits and the 14-day offline policy are unchanged.

## v1.0.0 (Initial Release)

**Released:** 2026/10/18 &nbsp;·&nbsp; **Requires:** Blender 5.1 (Minimum 5.1.1)

The first public release of Segment Display Pro.

### Input Categories

- **Numbers:** numeric readouts in Simple mode (up to 8 digits) or Complex mode (up to 15 digits across five input groups), with decimals and minus sign. Complex mode keeps long numbers accurate, with no rounding errors. See the [Troubleshooting page](troubleshooting.md#numbers).
- **Alphanumeric:** text and character readouts on up to 3 displays, with alignment options.
- **Time:** Clock, Timer and Date readouts. Can animate automatically in sync with the scene time (12/24-hour format, time direction, start offset).

### Display

- 7-segment and 16-segment display models.
- Segment Thickness, Segment Gap and Display Angle (straight to italic).
- 7-segment alternative fonts for the digits 6, 7 and 9.
- 16-segment Font Width (full/narrow), Font Align and Font Alternatives.
- Horizontal and vertical align, Display Size, digit and character spacing, Minus Sign Offset, Decimal Size and Decimal Vertical Position.
- Light-Emitting (LED) and Monochrome (LCD-style) display materials.

### Separators

- Whole and decimal separators (colons, dots, dashes and more), each configurable on its own.
- Digit-style separator character: uses a segment digit as a separator, with its own segment model, segment count and Segment Gap.
- Separators in between characters and displays.

### Viewport & Overlays

- **Solid Viewport Preview:** see LED segments in Solid shading.
- **Ghost Segments:** shows the inactive (unlit) segments in the viewport for easier layout. Useful if the LED Base is hidden or not toggled.
- **Z-Offset:** sets the gap between the LED segments and the display base. Also fixes flickering when the display is viewed from far away.

### Add-on

- "SegDisp Pro" tab in the 3D Viewport sidebar (N-panel).
- "Add Segment Display" button, adds the object at the 3D cursor.
- Fully procedural Geometry Nodes setup. All display objects share one linked asset file.
- Works with EEVEE and Cycles.
- License key activation and deactivation (Lemon Squeezy), 3 activation seats. Activation survives restarts, updates, reinstalls and new Blender versions (requires an online check at least every 14 days).
- **Offline license notices:** a red warning at the top of the N-panel and in Preferences during the last 3 days of the 14-day offline period, and when the add-on is locked. "Read more..." explains the steps and "Verify now" checks the license online right away.
- "Asset Status" section in Preferences with a "Re-link Asset" button.

### Known Limitations

!!! warning "Known Limitations"
    - Auto time animations only work with whole-number frame rates (24, 25, 30, 60, ...).
    - Only one Display Style is available for now. More styles are planned.
    - Harmless "VFont -> Node" warnings may appear in the System Console after reloading scripts or relinking assets.
    - Only tested on Windows 11 and Blender's default add-on folder.



