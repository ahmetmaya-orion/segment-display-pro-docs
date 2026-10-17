
All notable changes to Segment Display Pro are listed here, newest first.

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


