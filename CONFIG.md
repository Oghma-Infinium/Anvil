![](https://raw.githubusercontent.com/Oghma-Infinium/Anvil/refs/heads/main/Media/Anvil%20Header.png)

<p align="center">
  [  <a href="https://www.nexusmods.com/skyrimspecialedition/mods/147302">Nexus Page</a> | <a href="https://github.com/Oghma-Infinium/Anvil">Installation</a> | <a href="https://github.com/Oghma-Infinium/Anvil/blob/main/CHANGELOG.md">Changelog</a> |
  Configuration</a> |
  <a href="https://loadorderlibrary.com/lists/anvil">Load Order</a> | 
  <a href="https://discord.gg/4WwqfK5yHg">Modlist Discord</a> ]
</p>

---

- [Optional Addons](#optional-addons)
  - [Keyboard Keybinds](#keyboard-keybinds)
  - [Performance Optimizations](#performance-optimizations)
    - [Frame Generation](#frame-generation)
  - [Optional Visual Tweaks](#optional-visual-tweaks)
  - [Ultrawide Support](#ultrawide-support)
  - [Changing Resolution](#changing-resolution)

# Optional Addons

The following sections detail the **supported** modifications to the list. Any other modifications should be discussed in the `#Anvil-Modified` channel of the [Waking Dreams](https://discord.gg/4WwqfK5yHg) support server.

<sup>If you just want a place to talk with others about modifying the list, feel free to join! I'd be happy to help as well, all I ask is keeping it contained to that `#Anvil-Modified` channel<sup>

## Keyboard Keybinds

This section is going to be short, basic, and only go over the *additional modded keybinds*. All other controls, other than the ones listed below, are bound to vanilla keybinds.

Please refer the [this](https://ck.uesp.net/wiki/Input_Script) page for the DXScanCodes used by most mods if you'd like to change the binds for these mods **outside of the game**.

- [ReShade](https://reshade.me/): `Home` Key
    - ReShade Effects Toggle : `\` Key
- [Toggle UI](https://www.nexusmods.com/skyrimspecialedition/mods/112819): `F6` Key
    - Toggle Compass Only: `Right Shift + F6` Keys
    - Toggle Subtitles Only: `Right Ctrl + F6` Keys
- [Debug Menu](https://www.nexusmods.com/skyrimspecialedition/mods/136456): `F1` Key
- [Modex - A Mod Explorer Menu](https://www.nexusmods.com/skyrimspecialedition/mods/137877): `Delete` Key
- [Community Shaders](https://www.nexusmods.com/skyrimspecialedition/mods/86492): `End` Key
- [True Directional Movement](https://www.nexusmods.com/skyrimspecialedition/mods/51614)'s Target Lock: `M3` button (Scroll Wheel button)

## Performance Optimizations

>[!IMPORTANT]
>Make sure to set your CPU Affinity before experimenting with other Performance Optimizations below!
<Details>
<summary>Setting CPU Affinity</summary>

 1. Click the `Puzzle Piece` button at the top of MO2 and select `Set CPU Affinity` and press `OK` on the pop-up box.
 
    ![](https://raw.githubusercontent.com/Oghma-Infinium/Vagabond/main/images/cpu%20affinity%20example.png)
 2. That's it, it's really that simple. **Please, please, please** do this before launching the game and whenever you update the modlist.

</Details>

Below are the list of mods you will find under the `Performance Optimizations` separator in MO2.

 1. `Faster HDT-SMP - AVX512 Optimization`: This mod provides the AVX512 version of the [Faster HDT-SMP](https://www.nexusmods.com/skyrimspecialedition/mods/57339) `.dll`, optimized for CPUs supporting AVX-512. Highly suggested if your CPU supports it, but if you're unsure about compatibility, check your CPU specs online or with tools like HWinfo. **Using this mod on an incompatible CPU will crash your game or break all SMP.**
 2. `Anvil - Performance DynDOLOD Output`: If you want to squeeze out some easy performance improvements, I would highly suggest ticking this mod on and following the instructions below

    <Details>
    <summary>Instructions for swapping to this version of DynDOLOD</summary>

    1. **If swapping on an existing save game**, make a [clean save](https://dyndolod.info/Help/Clean-Save) (follow steps 1-4).
    2. Activate the `[Performance] Anvil - Performance DynDOLOD Output` mod under the **Performance Optimizations** separator in the left pane of MO2.
    3. Deactivate the `Anvil - DynDOLOD Output` mod under the **LOD Outputs** separator in the left pane of MO2.

    </Details>

### Frame Generation

By default, Community Shaders comes with Frame Generation enabled. I've disabled this option by default due to some hardware not supporting it. (I know most hardware should but it's disabled as a pre-cautionary)

If you have a GPU that supports DirectX 12 and a 120hz+ monitor, follow the instructions below to enable Frame Generation:

- Start up Anvil (Make sure you're actually in-game and not at the Main Menu)
- Press the `END` key to open the Community Shaders overlay
- Navigate to the `Display` section
- Switch the Frame Generation option to `Enabled`
- (Optional) **If you have a NVIDIA RTX GPU**, I really recommend switching the Upscaling Method slider to `NVIDIA DLAA` too
- Restart the game

If you do NOT have a 120hz+ monitor, you can still force enable Frame Generation with the `Force Enable Frame Generation` slider but I'm not liable for any issues you might get from doing so!

## Optional Visual Tweaks

This separator contains a series of visual-related tweaks.

 1. `Anvil - Arachnophobia and Entomophobia Support`: Removes some enemies that may trigger Arachnophobia or Entomophobia in some users.
 2. `Actually Brighter Lux Templates`: If interiors still feel too dark even after adjusting the in-game brightness slider, enable this mod to brighten them further.

## Ultrawide Support

Anvil offers some mods to provide Ultrawide and Widescreen Support. Under the **Ultrawide Support** Separator in MO2 you will find some mods that you will want to activate if you are playing on Ultrawide or Widescreen resolutions (21:9 or 32:9).

Please note that I (bingus) do not own a widescreen monitor. The additional ultrawide mods are mostly there out of courtesy for ultrawide users who want to play the list. If anyone would like to contribute to improvements for wltrawide support, please feel free to reach out!

</Details>

## Changing Resolution

By default, Wabbajack will set the resolution in the list's `Skyrimprefs.ini` to match the native resolution of your monitor. However, Skyrim scales very poorly at resolutions above 1080p (`1920x1080`) and depending on your hardware, it might be difficult to achieve consistent FPS on higher resolutions.

The preferable way to change your resolution is below:

- Click the `Data` tab on the right pane of MO2.
- In the filter bar at the bottom, type in `SSEDisplayTweaks.ini`
- Expand the folders, right-click `SSEDisplayTweaks.ini`, select "Open", and edit the following lines:
  - `#Resolution=1920x1080`
- After changing the resolution, remove the `#` in order for the settings to take affect when launching the game.

Example for how the .ini line should look:  
Before: `#Resolution=1920x1080`  
After: `Resolution=2560x1440`