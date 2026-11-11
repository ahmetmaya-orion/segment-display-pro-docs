# Introduction

Segment Display Pro is a procedural Blender add-on that lets you create fully customizable segment displays using Geometry Nodes. Inspired by the real electronic components found in digital clocks, calculators, speedometers, and control panels, it brings that distinct segmented aesthetic into your 3D and motion graphics projects without the hassle of manual modeling. All controls are exposed through a clean N-panel interface in the 3D View sidebar, so you can build and drive segment-style readings without leaving the viewport.

This manual covers everything you need to get started: installation, activation, the N-panel interface, and a detailed breakdown of every input and setting available to you. Whether you're building a retro dashboard or a sci-fi HUD, this guide will help you get the most out of the add-on.

!!! note "Note for Lite edition users:" 
     The Segment Display Lite edition does not have a separate user manual. However, Lite users can still reference this manual for the Installation, Activation, Troubleshooting, and Settings & Preferences sections, as they apply to both editions. **Exception: Lite's asset recovery procedure differs from Pro's and is not covered in this manual.** The remaining sections (such as Input Categories) cover Pro-specific features, but may still be useful as a general reference.

## What it does

Segment Display Pro provides a set of display modules that you place and control
from the N-panel. The available areas include:

- **Numbers** — numeric segment readouts.
- **Alphanumeric** — text and character displays.
- **Time** — clock, timer and date readouts.
- **Separators** — whole and decimal separator elements for composing layouts.
- **Display Options** — organize and switch between display groups.
- **Viewport overlays** — on-screen visual aids while working.
- **Add-on settings** — global preferences and options.

Each module is driven by the same underlying Geometry Nodes assets, so the
display geometry stays procedural and adjustable after creation.

## Add-on Credits & Requirements

| Item              | Requirement                                                  |
| ----------------- | ------------------------------------------------------------ |
| Full Name           | Segment Display Pro           |
| N-panel Label       | SegDisp Pro                   |
| Add-on version      | 1.0.0                         |
| Compatible Blender  | 5.1 (Minimum 5.1.1)           |
| Render Engines      | Eevee, Cycles                 |
| OS Platforms        | Windows*, Linux, macOS        |
| Location in UI      | `3D View` → Sidebar (`N`) → **SegDisp Pro** tab   |
| Add-on Type/Format  | Legacy/zip                     |
| Script Size         | 492 – 575 KB**                 |
| Asset Size          | 170 – 200 MB**                 |

!!! info "Important"
    * The Segment Display add-on was not developed for a specific operating system. However, it has only been tested on a Windows 11 system. Before purchasing the Pro edition, we recommend testing your system with the free Lite edition.
    
    ** File sizes may change over time with future updates.

## Where to find it in Blender

After the add-on is enabled, open the 3D Viewport and press `N` to show the
sidebar. Segment Display Pro appears under its own **SegDisp Pro** tab, alongside
Blender's other N-panel categories.

## The Asset File

When you add a display, its Geometry Nodes setup uses the .blend asset linked from the add-on's `assets` folder. Displays can share this library, including across scenes. If the asset is missing or its path changes, displays may appear as planes without their stored modifier settings being lost.

:material-tag-outline: **Pro v1.0.1 and later**

Preserve a project copy, reinstall the complete matching add-on and restart Blender first. Displays often reconnect automatically; if they are correct, no manual recovery is needed. If supported problems remain, use **Preferences > Add-ons > Segment Display Pro > Asset Status > Review & Recover…**. Reconnecting a library retains data still present; restoring an empty node-tree assignment and recreating a deleted modifier are different operations. Recreation uses defaults, not deleted settings or animation. See [Review & Recover](prefs_and_settings.md#review-recover).

!!! warning "Protect your project and shipped asset"
    Do not delete the linked library, remove node-tree assignments or rename/delete display modifiers as a repair shortcut. Recovery cannot guarantee restoration of missing settings or animation. Each edition controls its own objects; Pro recovery does not convert Lite objects.

    Do not open, modify, re-save, rename or move the shipped asset file. Re-saving changes its byte-level fingerprint even if it looks unchanged. Reinstall the original ZIP if it was altered. See [asset safety and recovery limits](troubleshooting.md#the-asset-file).

## The Segment Display Object

- The "Add Segment Display" button in the N-panel interface only appears when you click on an empty space in the 3D scene. The object is always added at the current **3D cursor** location.

- If you add a SegDisp object while the viewport is in **Solid** shading mode, you may not see the results of your inputs. Switch to **Material Preview** or **Rendered** shading, enable **Solid Viewport Preview** in the **Viewport & Overlays** panel, or disable/hide the **LED Base** to make the segment values visible. See [Troubleshooting: Viewport | Solid Color Preview](troubleshooting.md#viewport-solid-color-preview) for Solid viewport limitations and fixes.

- The N-panel always displays the settings of the active segment display object (the one with the brighter outline, i.e. the last one you clicked). You don't need it to be the only selected object; even if multiple objects are selected, the panel controls whichever segment display is active.

- The object settings will only appear if a Segment Display object is active or selected. If any other type of element is selected in the scene, a "Select a Segment Display object" message will be shown instead.

!!! info "Important"
    Each edition can only control objects created with that edition. SegDisp Pro cannot control SegDisp Lite objects, and SegDisp Lite cannot control SegDisp Pro objects. Use the matching add-on's N-panel to adjust each object.

## Licensing

Segment Display Pro is a commercial add-on. It uses license-key activation, so a
valid key is required to unlock the full feature set. See the [installation and
Activation](installation.md) pages for details.


