# Introduction

Segment Display Pro is a procedural Blender add-on that lets you create fully customizable segment displays using Geometry Nodes. Inspired by the real electronic components found in digital clocks, calculators, speedometers, and control panels, it brings that distinct segmented aesthetic into your 3D and motion graphics projects without the hassle of manual modeling. All controls are exposed through a clean N-panel interface in the 3D View sidebar, so you can build and drive segment-style readings without leaving the viewport.

This manual covers everything you need to get started: installation, activation, the N-panel interface, and a detailed breakdown of every input and setting available to you. Whether you're building a retro dashboard or a sci-fi HUD, this guide will help you get the most out of the add-on.

!!! note "Note for Lite edition users:" 
     The Segment Display Lite edition does not have a separate user manual. However, Lite users can still reference this manual for the Installation, Activation, Troubleshooting, and Settings & Preferences sections, as they apply to both editions. The remaining sections (such as Input Categories) cover Pro-specific features, but may still be useful as a general reference.

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

- When you add a segment display object to the scene via the N-Panel interface, the Segment Display asset blend file appears in Outliner > Blender File as linked. No matter how many segment display objects you have in the scene, they all share the same single linked asset data. 

!!! warning "Linked Blend Data"
    Do not delete the linked blend file directly from the Outliner — doing so will cause you to lose all your object settings. If you need to clean up your project file, make sure there are no segment display objects remaining in the scene, then use Blender > Purge Unused Data — this will automatically remove the asset file from the current blend file.

- If you accidentally uninstall the add-on, all your segment display objects will appear as planes on the next Blender launch, because the linked asset file is no longer available. The link directory information, however, is retained in the Blender file as a broken link. To restore everything, simply re-install the add-on and click the Re-link button in the Preferences > "Asset Status" panel — all your objects will be restored with their original settings.

!!! warning "Do not open or modify the asset file!"
    The add-on includes a .blend asset file. The add-on **links** to this file (it doesn't append it), so it has to stay exactly as shipped. Do not open, edit, re-save, rename or move it. Even opening and saving it in Blender without changing anything can break the add-on.

    **Why this matters for support:** every shipped asset file has its own unique ID (a digital fingerprint) that we use to check it's the original. Opening or re-saving the file, even without changing anything, breaks that ID. Think of it like a laptop warranty: once you open the case, it's no longer covered. If the asset file has been modified, we can't provide support until you reinstall the add-on from the original ZIP.

    If displays start acting strange or won't load, uninstall the add-on and reinstall it from the original ZIP.

## The Segment Display Object

- The "Add Segment Display" button in the N-panel interface only appears when you click on an empty space in the 3D scene. The object is always added at the current **3D cursor** location.

- The N-panel always displays the settings of the active segment display object (the one with the brighter outline, i.e. the last one you clicked). You don't need it to be the only selected object; even if multiple objects are selected, the panel controls whichever segment display is active.

- The object settings will only appear if a Segment Display object is active or selected. If any other type of element is selected in the scene, a "Select a Segment Display object" message will be shown instead.

!!! info "Important"
    Each edition can only control objects created with that edition. SegDisp Pro cannot control SegDisp Lite objects, and SegDisp Lite cannot control SegDisp Pro objects. Use the matching add-on's N-panel to adjust each object.

## Licensing

Segment Display Pro is a commercial add-on. It uses license-key activation, so a
valid key is required to unlock the full feature set. See the [installation and
Activation](installation.md) pages for details.

