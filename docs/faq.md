# Frequently Asked Questions

Quick answers to the most common questions about Segment Display Pro and Segment Display Lite.

## The Lite Edition

???+ question "Is there a free version of the Segment Display add-on?"
    
    Yes. There is a free version of the add-on called "Segment Display Lite". The Lite version is not a demo product. It's just a simplified variant with some limited features compared to the Pro version, for anyone who wants to discover the add-on. You can review the [Edition Features Table](edition_features.md) to compare both versions.

??? question "Does Segment Display Lite have a time trial period?"
    
    No, the free version has no time trial. You can use it until a large asteroid hits the Earth!


??? question "Will the Lite version receive updates in the future?"
    
    No. For major future updates and releases, we focus all our efforts on the Pro version. The Lite version will only receive occasional hotfix patches.


??? question "Are the Lite and Pro versions independent add-ons?"
    
    Yes, they are completely different add-ons; both editions have their own assets and plugins. You do not have to install the Pro version on top of the Lite version. Both can be used on the same system. Keep in mind that you cannot control a Lite object through the Pro N-panel interface, and vice versa.

## Installation & Updates

??? question "Which Blender versions are supported?"
    
    :material-tag-outline: **v1.0.1 and later**

    SegDisp v1.0.1 has been tested with **Blender 5.1.2**, the recommended version for this release. The declared minimum is **Blender 5.1.1**, but v1.0.1 has not yet been re-tested on that version. Newer Blender versions are not confirmed as supported yet. The add-on runs on Windows, macOS and Linux (tested on Windows 11 only), and works with both the Cycles and EEVEE render engines. If a future add-on update needs a newer Blender version, the add-on will notify you. See the [Installation & Activation](installation.md#requirements) page for the full system requirements.


??? question "How do I update the add-on without losing my activation?"

    Install the complete matching ZIP over the old version with Target Path set to Default and Overwrite enabled, then restart Blender. Your activation file is outside the add-on folder. Reopen and inspect your project first: displays often return automatically. For Pro v1.0.1 and later, use **Review & Recover…** only if supported issues remain after the installed asset is available. See [Updating the Add-on](installation.md#updating-the-add-on).

??? question "Does Check for Updates install the update?"

    :material-tag-outline: **v1.0.1 and later**

    No. **Check for Updates** only checks whether a newer version is available. If there is one, **Open Downloads** opens the download page in your browser. Nothing is downloaded, installed or restarted for you. Download the new ZIP, install it over your current version, then restart Blender. See [Add-on Update](prefs_and_settings.md#add-on-update) and [Updating the Add-on](installation.md#updating-the-add-on).

??? question "How do I repair displays after an update or reinstall?"

    :material-tag-outline: **Pro v1.0.1 and later**

    If displays appear as planes, preserve a project copy and leave their modifiers untouched. Reinstall the complete matching add-on and restart Blender first; this often restores displays without manual recovery. If problems remain, use **Preferences > Add-ons > Segment Display Pro > Asset Status > Review & Recover…**. Review the actions and backup option, recover, inspect settings/animation and save.

    Reconnection uses data still present. Deleted settings and animation cannot be restored by assigning a node tree again or recreating a modifier with defaults. Lite uses a different recovery procedure, not covered here. See [Review & Recover](prefs_and_settings.md#review-recover).

??? question "Why is Add unavailable after updating?"

    Restart Blender first, then check Asset Status. **Not Available** means the installed asset cannot be used; **Unknown** version information needs checking, and a known asset/add-on version mismatch can block adding displays. Reinstall the complete matching package rather than mixing asset/script versions or editing modifiers. See [asset troubleshooting](troubleshooting.md#the-asset-file).

??? question "Why did Blender stop responding during recovery?"

    Blender can pause while recovery relocates and reloads an asset library whose path points outside the current installation. Allow it to finish; duration varies and a temporary not-responding message does not necessarily mean a crash. This involves Blender's library handling; the exact bottleneck is unconfirmed. See [recovery pauses](troubleshooting.md#blender-temporarily-stops-responding).

## Licensing & Usage

??? question "Does the add-on require a license key to be activated?"

    Yes. Both the Lite and Pro versions require license activation through your Lemon Squeezy account. After purchasing, you'll need to activate your license key to use the add-on. You can manage your license and activations directly from your Lemon Squeezy account dashboard.

??? question "How many devices can I activate my license on?"

    Each Segment Display Pro license key includes 3 activations (Segment Display Lite includes 1). Every time you activate the add-on on a new device, it counts toward your limit. If you need to move your license to a different machine, make sure to deactivate it on the old device first.

    !!! warning "Important"
        Uninstalling the add-on without deactivating does not free up the activation slot. If you accidentally uninstall without deactivating, you can free up the slot yourself from your <a href="https://app.lemonsqueezy.com/my-orders" target="_blank" rel="noopener">Lemon Squeezy order dashboard</a>.

??? question "Does the add-on work on render farms?"

    Your own render machines, yes. Your Pro license comes with 3 activation seats, so you can use it on your main workstation, a laptop, and a dedicated render machine. Every machine that renders your scene needs Segment Display Pro installed in Blender's default add-on folder, using the same Blender version, and its own activation (the license file can't be copied between machines). Cloud render farms that don't let you install add-ons are not supported.

??? question "Can I use the add-on in commercial projects?"

    Yes. Segment Display Pro uses a dual license:

    - **Add-on code (GPL v3):** You're free to use, copy, and modify the code for your own pipeline. If you distribute a modified version, you must pass on the same freedoms and source code.
    - **Assets (Single User Commercial License):** The .blend files, 3D models, and textures remain the property of Orion November Studio. You can use them to produce videos and animations for commercial use and to build your personal portfolio. You can't sell, share, sub-license, or upload the assets, in original or modified form, as standalone files or as part of another tool or add-on.

    In short: your renders are yours to sell, the asset files are not. Full details are in our <a href="https://www.orionnovemberstudio.com/integrated-governance-and-license-framework" target="_blank" rel="noopener">license terms</a>.

## Add-on In Action

??? question "Why does the add-on link assets instead of appending them to the scene?"

    The Segment Display Geometry Nodes asset references numerous external objects and collections required for correct functionality. Appending the asset would automatically import all of those external objects into the scene, with no way to preserve the original collections and sub-collections hierarchy, leaving the Outliner cluttered and difficult to manage. Linking also offers an additional advantage: any future updates made to the asset in the source file are automatically reflected in the scene, eliminating the need to re-import.

??? question "What are the segdisp_* custom properties on my Pro object?"

    They are recognition/recovery metadata, not display controls. Leave `segdisp_type`, `segdisp_schema`, `segdisp_edition` and `segdisp_modifier` intact, and do not manually rename/delete the SegDisp modifier. An object's identity does not always identify its correct empty modifier; ambiguous targets require **Needs Review**. See [recognition properties](troubleshooting.md#pro-recognition-properties-and-modifiers).

??? question "Why are segment value results not shown in solid shading mode when the display base is toggled?"

    The LED part of the segment display object is a solid mesh aligned over the display base and visible via an emission material, which is not noticeable in solid mode. If you want to see the value results, you may have to switch to the material or rendered view. However, if you are working in a busy scene and don't want to lose viewport performance, you can toggle the "Solid Viewport Preview" button in the "Viewport & Overlays" add-on panel to see the results in solid view. See [Viewport & Overlays](viewport_overlays.md) for details.

    !!! info
        The Solid Viewport Preview sets the viewport object color to "Attribute (Vertex)", which affects the entire scene.

??? question "Why are there two different options for the Numbers category?"

    Blender stores number inputs as single-precision floats (float32), which limit the precision of a single input. SegDisp Pro's Simple input supports values up to **10,000,000**; an 8-digit display does not mean every 8-digit value is supported.

    That's why the Numbers category offers two input options:

    - **Simple:** A single input field for everyday values, with up to 8 display digits and a maximum input value of **10,000,000**.
    - **Complex:** Builds the current number from five three-digit input groups, each accepting **0-999**, for up to **15 display digits**. These are not fixed decimal or place-value separator groups. Display Length determines which groups remain active, while Decimals and Decimal Length determine decimal formatting. The rightmost group [1] remains active for whole numbers when Decimals is off.

    See the [Troubleshooting](troubleshooting.md#numbers) page for details.

## Animation & Rendering

??? question "Can I animate the display values?"

    Yes. Most N-panel inputs can be keyframed like any other Blender property: hover over a value and press I. The Time category also includes built-in auto animations (Clock and Timer), so you don't have to keyframe anything for clocks and countdowns. Since Blender can't animate text inputs, the Alphanumeric category uses a built-in multi-input preset system to switch between words over time. See the [Alphanumeric](in_cat_alphanum.md) page for more details.

??? question "Does it render in both Cycles and EEVEE?"

    Yes, both engines are supported. In EEVEE, enable Raytracing in Properties > Render Properties so the segment emission lights up the scene the way it does in Cycles. More tips are on the [Troubleshooting](troubleshooting.md#eevee-render-engine-tips) page.

??? question "Why is my timer drifting at 29.97 fps?"

    The auto time animations (Clock, Timer), including **Clock Start Frame** and **Timer Start Frame**, only work correctly with whole-number frame rates such as 24, 25, 30, or 60. Decimal frame rates like 23.98 or 29.97 cause small timing errors because of how Blender converts frames to time. Also, make sure the "Addon Frame Rate" dropdown in the N-panel matches your scene's frame rate. See the [Preferences & Settings](prefs_and_settings.md#time-synchronization) page for details.

## Sharing & Exporting

??? question "Can I link a SegDisp object from another project?"

    This workflow is not currently validated. Configure and animate displays in their owning project; repair and save that source before reloading its library in the destination. Recovery does not directly edit source-linked modifiers. Lite testing showed input-type errors after library reload; restarting cleared the observed error but is not a guaranteed fix or a confirmed Pro defect. Linked-object still and animation rendering remain unverified. See [linking limitations](troubleshooting.md#linking-displays-from-another-project).

??? question "Can I share my .blend file with someone who doesn't own the add-on?"

    Your renders and videos are yours to share with anyone. The .blend project itself is a different story: Segment Display objects link to the asset file inside the add-on installation, so on a computer without Segment Display Pro they show up as flat planes. A teammate who owns their own copy of Segment Display Pro can open and edit your project normally (Lite can't open Pro objects). Since the assets are covered by a single-user license, they can't be shared inside a .blend file in original, converted, or modified form.

??? question "Can I export to Unity, Unreal or FBX?"

    Not in the current version. Segment Display Pro is built for rendering inside Blender: the displays are generated procedurally with Geometry Nodes and linked assets, which can't be exported to other software with their animation. Exporting the assets as models for use in games or other tools would also fall outside the asset license, which only covers videos, animations, and portfolio work made in Blender.
