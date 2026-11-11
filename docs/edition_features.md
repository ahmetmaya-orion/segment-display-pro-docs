# Edition Features Table

A side-by-side look at what ships in **Segment Display Pro** and **Segment Display Lite**.

| Feature | LITE | PRO |
| ------- | ---- | --- |
| **GENERAL** | | |
| License Activation Seats | 1 activation | 3 activation |
| Future Updates/Upgrades | Hotfixes Only | ✓ |
| Add-on Support | Social | E-mail |
| Documentation | Reference Only | Full |
| **NUMBERS** | | |
| Input Options | Simple | Simple / Complex |
| Display Length | 6 | 8 / 15 |
| Toggle Decimals | ✓ | ✓ |
| Decimal Length | 2 | 4 / 8 |
| Place Value Separation | ✓ | ✓ |
| Hide Leading Zeros | ✕ | ✓ |
| Numbers Left Align | ✕ | ✓ |
| **TIME** | | |
| Time Options | Clock / Date | Clock / Timer / Date |
| Toggle Seconds | ✓ | ✓ |
| Clock Time Format | ✓ | ✓ |
| Clock Animation | Auto (Scene Time) | Auto / Manual \| Time Direction |
| Timer Options | ✕ | ✓ |
| Date Format | ✓ | ✓ |
| Date - Month Format | ✕ \* | ✓ |
| Date - Year Format | ✓ | ✓ |
| **ALPHANUMERIC** | | |
| Display Count | Single | Up to 3 |
| Display Length | 6 | 16 |
| Input Align | ✓ | ✓ |
| Input Options | Single Input | Single / Multi (Presets) Input |
| Separators In Between \*\* | Characters | Characters / Displays |
| **SEPARATORS** | | |
| Characters | 3 | 7 |
| Shapes | 2 | 5 |
| Shape Options | Limited | Full |
| Separators In Between \*\* | Characters | Characters / Displays |
| **DISPLAY** | | |
| Segment Display Models | 7-Segment | 7 / 16 Segment |
| Model Styles | Single | Single \*\*\* |
| Segment Fonts | Numbers Only | Numbers & Alphabet |
| Appearances | ✓ | ✓ |

**\*** Month format: Numbers or alphanumeric. The alphanumeric format is only compatible with the 16-segment display model, which is only included in the Pro version.

**\*\*** Locate the "Separators" panel. Because of the alphanumeric display count limitation in the Lite version, this feature is only available in Segment Display Pro.

**\*\*\*** More styles will be available in future updates for Segment Display Pro.

## Asset Recovery

:material-tag-outline: **v1.0.1 and later**

| Capability | LITE | PRO |
| ---------- | ---- | --- |
| Recovery interface | Simplified Re-link Asset | Review & Recover preview |
| Supported library reconnection | Limited project-wide Re-link | Selectable library reconnection across scenes |
| Supported missing node-tree assignments | Limited identification-based recovery | Restore Node Tree; ambiguous targets require review |
| Recreate a deleted modifier | Not supported | Opt-in for qualifying marked objects, using defaults |
| Saved-project backup option in recovery dialog | No Pro recovery dialog | Available; requested backup failure cancels recovery |
| Numeric-toggle input repair | No Pro selectable repair preview | Supported toggle repair retaining on/off values |
| Direct repair of source-linked modifiers | No | No |

Reconnection uses data still present; deleted settings and animation are not restored by assigning a tree or creating a default modifier. Reinstalling the matching add-on and restarting Blender may restore displays without manual recovery. Lite's recovery procedure is not covered in this manual. See [Pro Review & Recover](prefs_and_settings.md#review-recover).
