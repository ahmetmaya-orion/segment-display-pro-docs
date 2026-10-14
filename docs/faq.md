# Frequently Asked Questions

Quick answers to the most common questions about Segment Display Pro and Segment Display Lite.

## The Lite Edition

**Is there a free version of the Segment Display add-on?**

Yes. There is a free version of the add-on called "Segment Display Lite". The Lite version is not a demo product. It's just a simplified variant with some limited features compared to the Pro version, for anyone who wants to discover the add-on. You can review the [Edition Features Table](edition_features.md) to compare both versions.

**Does Segment Display Lite have a time trial period?**

No, the free version has no time trial. You can use it until a large asteroid hits the Earth!

**Will the Lite version receive updates in the future?**

No. For major future updates and releases, we focus all our efforts on the Pro version. The Lite version will only receive occasional hotfix patches.

**Are the Lite and Pro versions independent add-ons?**

Yes, they are completely different add-ons; both editions have their own assets and plugins. You do not have to install the Pro version on top of the Lite version. Both can be used on the same system. Keep in mind that you cannot control a Lite object through the Pro N-panel interface, and vice versa.

## Installation & Updates

**Which Blender versions are supported?**

Segment Display Pro v1.0.0 is built for Blender 5.1, with Blender 5.1.1 as the minimum version. It runs on Windows, macOS and Linux, and works with both the Cycles and EEVEE render engines. If a future add-on update needs a newer Blender version, the add-on will notify you. See the [Installation & Activation](installation.md#requirements) page for the full system requirements.

**How do I update the add-on without losing my activation?**

Just install the new ZIP right over the old one; no need to uninstall first. Use "Install from Disk" with "Target Path" set to "Default" and "Overwrite" ticked, then restart Blender. Your license stays activated because the license file is stored outside the add-on folder and updates never touch it. If your Segment Display objects don't come back after the restart, click "Re-link Asset" in Preferences > Add-ons > Segment Display Pro > "Asset Status". See [Updating the Add-on](installation.md#updating-the-add-on) for details.

## Licensing & Usage

**Does the add-on require a license key to be activated?**

Yes. Both the Lite and Pro versions require license activation through your Lemon Squeezy account. After purchasing, you'll need to activate your license key to use the add-on. You can manage your license and activations directly from your Lemon Squeezy account dashboard.

**How many devices can I activate my license on?**

Each Segment Display Pro license key includes 3 activations (Segment Display Lite includes 1). Every time you activate the add-on on a new device, it counts toward your limit. If you need to move your license to a different machine, make sure to deactivate it on the old device first.

!!! warning "Important"
    Uninstalling the add-on without deactivating does not free up the activation slot. If you accidentally uninstall without deactivating, you can free up the slot yourself from your <a href="https://app.lemonsqueezy.com/my-orders" target="_blank" rel="noopener">Lemon Squeezy order dashboard</a>.

**Does the add-on work on render farms?**

Your own render machines, yes. Your Pro license comes with 3 activation seats, so you can use it on your main workstation, a laptop, and a dedicated render machine. Every machine that renders your scene needs Segment Display Pro installed in Blender's default add-on folder, using the same Blender version, and its own activation (the license file can't be copied between machines). Cloud render farms that don't let you install add-ons are not supported.

**Can I use the add-on in commercial projects?**

Yes. Segment Display Pro uses a dual license:

- **Add-on code (GPL v3):** You're free to use, copy, and modify the code for your own pipeline. If you distribute a modified version, you must pass on the same freedoms and source code.
- **Assets (Single User Commercial License):** The .blend files, 3D models, and textures remain the property of Orion November Studio. You can use them to produce videos and animations for commercial use and to build your personal portfolio. You can't sell, share, sub-license, or upload the assets, in original or modified form, as standalone files or as part of another tool or add-on.

In short: your renders are yours to sell, the asset files are not. Full details are in our <a href="https://www.orionnovemberstudio.com/integrated-governance-and-license-framework" target="_blank" rel="noopener">license terms</a>.

## Add-on In Action

**Why does the add-on link assets instead of appending them to the scene?**

The Segment Display Geometry Nodes asset references numerous external objects and collections required for correct functionality. Appending the asset would automatically import all of those external objects into the scene, with no way to preserve the original collections and sub-collections hierarchy, leaving the Outliner cluttered and difficult to manage. Linking also offers an additional advantage: any future updates made to the asset in the source file are automatically reflected in the scene, eliminating the need to re-import.

**Why are segment value results not shown in solid shading mode when the display base is toggled?**

The LED part of the segment display object is a solid mesh aligned over the display base and visible via an emission material, which is not noticeable in solid mode. If you want to see the value results, you may have to switch to the material or rendered view. However, if you are working in a busy scene and don't want to lose viewport performance, you can toggle the "Solid Viewport Preview" button in the "Viewport & Overlays" add-on panel to see the results in solid view. See [Viewport & Overlays](viewport_overlays.md) for details.

!!! info
    The Solid Viewport Preview sets the viewport object color to "Attribute (Vertex)", which affects the entire scene.

**Why are there two different options for the Numbers category?**

Blender stores number inputs as single-precision floats (float32), which can only hold about 7 significant digits. Beyond that, even whole integers get rounded, so a long number typed into a single field would show wrong digits on the display.

That's why the Numbers category offers two input options:

- **Simple:** A single input field for everyday values, up to 8 digits.
- **Complex:** The number is split into five three-digit groups (0 to 999), one for each place value (ones, thousands, millions, billions, trillions). Each group stays well within Blender's safe precision range, and the add-on procedurally combines them on the display. This lets you show numbers up to 15 digits (hundred trillions) without any precision loss.

See the [Troubleshooting](troubleshooting.md#numbers) page for details.

## Animation & Rendering

**Can I animate the display values?**

Yes. Most N-panel inputs can be keyframed like any other Blender property: hover over a value and press I. The Time category also includes built-in auto animations (Clock and Timer), so you don't have to keyframe anything for clocks and countdowns. Since Blender can't animate text inputs, the Alphanumeric category uses a built-in multi-input preset system to switch between words over time. See the [Alphanumeric](in_cat_alphanum.md) page for more details.

**Does it render in both Cycles and EEVEE?**

Yes, both engines are supported. In EEVEE, enable Raytracing in Properties > Render Properties so the segment emission lights up the scene the way it does in Cycles. More tips are on the [Troubleshooting](troubleshooting.md#eevee-render-engine-tips) page.

**Why is my timer drifting at 29.97 fps?**

The auto time animations (Clock, Timer) and the Animation Start Offset only work correctly with whole-number frame rates such as 24, 25, 30, or 60. Decimal frame rates like 23.98 or 29.97 cause small timing errors because of how Blender converts frames to time. Also, make sure the "Addon Frame Rate" dropdown in the N-panel matches your scene's frame rate. See the [Preferences & Settings](prefs_and_settings.md#time-synchronization) page for details.

## Sharing & Exporting

**Can I share my .blend file with someone who doesn't own the add-on?**

Your renders and videos are yours to share with anyone. The .blend project itself is a different story: Segment Display objects link to the asset file inside the add-on installation, so on a computer without Segment Display Pro they show up as flat planes. A teammate who owns their own copy of Segment Display Pro can open and edit your project normally (Lite can't open Pro objects). Since the assets are covered by a single-user license, they can't be shared inside a .blend file in original, converted, or modified form.

**Can I export to Unity, Unreal or FBX?**

Not in the current version. Segment Display Pro is built for rendering inside Blender: the displays are generated procedurally with Geometry Nodes and linked assets, which can't be exported to other software with their animation. Exporting the assets as models for use in games or other tools would also fall outside the asset license, which only covers videos, animations, and portfolio work made in Blender.
