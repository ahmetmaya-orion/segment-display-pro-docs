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

| What you can do | LITE | PRO |
| --------------- | ---- | --- |
| Recovery tool | Simple **Re-link Asset** button | **Review & Recover** panel that previews every fix |
| Reconnect the asset file | Re-links the whole project in one go | You pick which library to reconnect, across all scenes |
| Reconnect a display's missing node setup | Basic: only displays it can recognize | **Restore Node Tree**; asks you to confirm when it isn't sure which modifier to fix |
| Rebuild a deleted SegDisp modifier | No | Optional, only for SegDisp objects, rebuilt with default settings |
| Back up your project before recovery | No (Lite has no recovery dialog) | Yes; if the backup fails, recovery stops and nothing changes |
| Fix on/off switches that turned into number fields | No | Yes, and it keeps your on/off choices |
| Fix displays linked from another .blend file | No | No (fix them in the original file) |

Recovery only reconnects what's still in your file. It can't bring back deleted settings or animation.

**Tip:** Reinstalling the matching add-on version and restarting Blender often fixes displays without any recovery.

Lite's recovery steps aren't covered in this manual. See [Pro Review & Recover](prefs_and_settings.md#review-recover).
