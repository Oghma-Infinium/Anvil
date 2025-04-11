![](https://raw.githubusercontent.com/Oghma-Infinium/Anvil/refs/heads/main/Media/Anvil%20Banner.png)

<p align="center">
  [ Installation | <a href="https://github.com/Oghma-Infinium/Anvil/blob/main/CHANGELOG.md">Changelog</a> |
  <a href="https://github.com/Oghma-Infinium/Anvil/blob/main/CONFIG.md">Configuration</a> | 
  <a href="https://loadorderlibrary.com/lists/anvil">Load Order</a> |
  <a href="https://discord.gg/4WwqfK5yHg">Modlist Discord</a> ]
</p>

---

**Modlist Support: [Waking Dreams](https://discord.gg/4WwqfK5yHg)**

>[!IMPORTANT]
>Anvil requires the four free AE mods (Fishing, Rare Curios, Survival Mode, and Saints and Seducers) included in the Skyrim Anniversary Edition update from November 2021

>[!WARNING]
>You must update Skyrim SE to the latest version (1.6.1170) on Steam to install this list.

# Table of Contents

- [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
    - [System Requirements](#system-requirements)
  - [Installation](#installation)
    - [Pre-Installation](#pre-installation)
      - [Installing Microsoft Visual C++ and .NET](#installing-microsoft-visual-c-and-net)
      - [Pagefile and Crash Prevention](#pagefile-and-crash-prevention)
      - [Setting Shader Cache Size (NVIDIA Users Only)](#setting-shader-cache-size-nvidia-users-only)
      - [Steam Setup](#steam-setup)
      - [Changing the Game Language](#changing-the-game-language)
      - [Installing Rare Curios Files](#installing-rare-curios-files)
    - [Wabbajack Installation](#wabbajack-installation)
      - [Installing Wabbajack](#installing-wabbajack)
      - [Downloading and Installing Anvil](#downloading-and-installing-anvil)
    - [Problems with installation](#problems-with-installation)
      - [Missing Manual Downloads](#missing-manual-downloads)
  - [Post-Installation and Optional Setup](#post-installation-and-optional-setup)
    - [Stock Game](#stock-game)
    - [Antivirus Exceptions](#antivirus-exceptions)
    - [Post-Installation Issues and Troubleshooting](#post-installation-issues-and-troubleshooting)
    - [Keyboard Keybinds](#keyboard-keybinds)
  - [Playing the Game](#playing-the-game)
  - [Updating the modlist](#updating-the-modlist)
  - [Removing the Modlist](#removing-the-modlist)
  - [Issues](#issues)
  - [Credits and Thanks](#credits-and-thanks)

## Introduction

**Anvil** is a visuals-only modlist for Skyrim Special Edition (1.6.1170) that is built around [Community Shaders](https://www.nexusmods.com/skyrimspecialedition/mods/86492). Originally crafted by Althro, it's now maintained by Bingus (former author of the [Ascensio](https://github.com/Oghma-Infinium/Ascensio) modlist) as my own personal playground for Community Shaders related mods. So whether you’re looking for a solid visual foundation to build upon or simply want to dive in and play as is, Anvil has you covered.

Every tweak and change is mostly documented within the `Notes` section of Mod Organizer 2, making it easy to keep track of what’s been adjusted. A heads-up for anyone checking out older videos or reviews: starting with versions 3.0+, I (bingus) have revamped Anvil to reflect my personal visual preferences, so much of the earlier content might not be accurate anymore.

A full list of the mods used in this modlist can be viewed [here](https://loadorderlibrary.com/lists/anvil).

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

### System Requirements

The section below outlines my *recommended* system specifications for the list. Please keep in mind that every PC is different, and these recommendations are mostly a guesstimate based on what I've monitored and firsthand reports. Individual performance may vary depending on specific hardware and software configurations, as well as other system optimizations. **Troubleshooting & support for hardware related issues will not be provided.**

>[!WARNING]
>
>- An SSD is **required** to the play the modlist.
>- Only Windows 10 or 11 operating systems are supported. Windows LTSC, special variants, lightened editions or any other modified variant **WILL NOT BE SUPPORTED.** Linux installations also **WILL NOT BE SUPPORTED**.

| Component | My Specs (1080p) | Recommended Specs (1080p) |
| :---         |:---:      |          ---: |
| CPU  | R7 7800x3D    | R7 5800x or Equivalent|
| GPU    | RTX 4080 SUPER | RTX 3060ti or Equivalent|
| Memory   | 32GB RAM | 16GB RAM or Greater |
| Storage  | NVME SSD | SATA SSD |

</Details>

Downloads Size: ~78 GB
Install Size: ~115 GB  
Temporary Files: ~30 GB  
**TOTAL:** ~193 GB  

> In case of a disparity between the listed sizes here and the Wabbajack Gallery, the values here should be more correct as Wabbajack does not properly account for archive compression in the post-installation list.

## Installation

Installing Anvil is relatively easy and, if you have Nexus Premium, will be a simple waiting game. If you are updating the modlist, you can safely skip to the [updating section](#updating-the-modlist).

### Pre-Installation

These steps are only required for installing the modlist for the first time. Additionally, many of these steps may be covered in other modlist installs, for new users I suggest reading through here regardless.

#### Installing Microsoft Visual C++ and .NET

 1. Install [Visual C++ x64](https://aka.ms/vs/17/release/vc_redist.x64.exe).
 2. Install [.NET Runtime 9.X.X Desktop x64](https://dotnet.microsoft.com/en-us/download/dotnet/9.0).
 3. Install [.NET 6.0 Runtime Desktop x64](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-desktop-6.0.30-windows-x64-installer).

>[!WARNING]
>If you already have Visual C++ installed, please make sure you install it again and use the `Repair` option to get the latest version of the redistributables. **Do NOT skip this step or MO2 and the game may fail to launch.**

#### Pagefile and Crash Prevention

>[!WARNING]
>Larger Skyrim modlists require a significant amount of memory, running out of memory **will** result in crashes and other potential issues.

**To set up a Pagefile:**

 1. Press `Win Key + R`
 2. Type `sysdm.cpl ,3` and hit `ENTER`
 3. Navigate to **Performance** and click the box `Settings...`
 4. Click the **Advanced** tab at the top
 5. Under **Virtual Memory** click the box `Change...`
 6. Uncheck `Automatically Manage` if it is checked
 7. Select your disk drive, ideally your fastest solid state drive
 8. Click `Custom Size:`
 9. In the box next to **Initial Size (MB)**, type `20480`
 10. In the box next to **Maximum Size (MB)**, type `20480`
 11. Click `Set`.
 12. Click `OK`.
 13. Click `Apply`.
 14. Click `OK`.
 15. **Restart your PC**.

>[!TIP]
> Your pagefile does not need to be on the same drive as your Wabbajack install or Steam install.

<Details>
<summary>Why do we need a Pagefile?</summary>

Skyrim is a very old game (originally released in 2011) that is built on the [Creation Engine](https://en.wikipedia.org/wiki/Creation_Engine), a engine based off of the [Gamebryo](https://en.wikipedia.org/wiki/Gamebryo) engine that was originally used for Morrowind (released in 2002, *before I was born*).  

Through lots of experience and trial-and-error, we have discovered that increasing the window's pagefile can fix certain types of Skyrim crashes, the two most common examples being `Unhandled native exception occurred at 0x7FF6ADC8DDDA` and `Unhandled native exception occurred at 0x0`.  

But why is this? Skyrim appears to use system memory in very unexpected ways, for example it will frequently dip into the pagefile memory despite there being available RAM. Skyrim heavily favors high speed, low latency RAM (the best you can get as of writing this is 6000MHz and CL30 for DDR5).  

</Details>

#### Setting Shader Cache Size (NVIDIA Users Only)

>[!IMPORTANT]
>For NVIDIA users, it is recommended to boost the size of the shader cache. These settings have been shown to improve stability, while it may not be entirely necessary, it is still recommended.

**To do this:**

- Right-click on your desktop and select `NVIDIA Control Panel`
- Navigate and click `Manage 3D Settings`
- Scroll down the **Global Settings** tab until you see **Shader Cache Size**
- Double-click `Driver Default` to the right of **Shader Cache Size** and select `10 GB`
- Click `Apply` in the bottom right hand corner
- Exit out of the application
![](https://raw.githubusercontent.com/iAmMe27/Tahrovin/main/img/ShaderCache.png)

#### Steam Setup

>[!WARNING]
>If you have your Steam Library in Program Files and only have one drive, please read [this article](https://github.com/LostDragonist/steam-library-setup-tool/wiki/Usage-Guide) by LostDragonist. Locations such as Desktop, Documents, Downloads, OneDrive, etc. *will* cause issues with installing and playing the list.

 1. Change Skyrim SE's Steam settings so it does not [automatically update](https://help.steampowered.com/en/faqs/view/71AB-698D-57EB-178C#disable).
 2. Please ensure you follow the steps outlined in the [Installing Rare Curios Files](#installing-rare-curios-files) section. Most AE DLC owners should not have to do this step but as a precautionary, please **DO NOT** skip this step.

#### Changing the Game Language

>[!WARNING]
>**The English Steam version of Skyrim SE is the only supported version.**

I understand that this may be frustrating for non-English speaking users or users with the GOG/Bethesda.net versions, but due to the core file differences between the different versions, I am only able to support one game version.

To change your Skyrim SE's language:

 1. Right click on Skyrim SE in Steam
 2. Click `Properties`
 3. Click `Language`
 4. Set the Language to `English`

#### Installing Rare Curios Files
>
>[!WARNING]
> ***Do NOT skip this step or your install may fail!***

Since the 1.6.1130 update (January 17, 2024), Steam has begun including the free Creation Club (CC) files with the base installation of Skyrim. However, these files do not have the same file hash as the files that are downloaded from the in-game **Creations** menu for Anniversary Edition (AE) users. In order to comply with Wabbajack policy and minimize issues for users who own the AE update, Anvil is compiled using the versions of the CC content that are obtained from the in-game **Creations** menu.  

As a result of this, for users who do not own the AE, you must ensure that you download the correct version of the CC files. Steps below:

 - Navigate to your Skyrim SE's Steam Data folder
    - i.e. `D:\SteamLibrary\steamapps\common\Skyrim Special Edition\data`
 - Delete *both* Rare Curios files:
    - `ccbgssse037-curios.bsa`
    - `ccbgssse037-curios.esl`
 - Launch Skyrim SE from Steam and select **Creations** at the main menu
 - Select **Search** at the bottom and search for `Rare Curios`
 - Select the card titled `Rare Curios` and press **Download**
 - Once it is done, accept Bethesda's load order message and exit the game

![](https://cdn.discordapp.com/attachments/1008055818782003421/1263168806054920283/Rare_Curios.png?ex=673cbb1f&is=673b699f&hm=1f79621666901b9b4fd93a5a1eb0732779388c4fa3fe4bb77d2211ffb6ab881b&)

>[!IMPORTANT]
>
>- **DO NOT** Alt+Tab during this process or it will fail to properly download these files.
>- **DO NOT** verify your game files after doing the steps above as it will revert the "correct" file hashes for the CC files you downloaded in this step.

### Wabbajack Installation

#### Installing Wabbajack

Once you have completed the pre-installation section, follow these steps to install Wabbajack:

1. Create an empty folder named `Wabbajack` on the root of your drive, such as `C:\Wabbajack` for example.
    > - **DO NOT place it in Program Files, User folders (such as Desktop, Documents, Downloads, OneDrive, etc.), in your Skyrim's Steam folder, or in any folders related to the modlist itself (the downloads or install folder).**
    > - The `Wabbajack` folder does not need to be on an SSD, but it makes installing faster. You can set this location to be on an HDD for the sake of saving space.

2. Download the [latest version of Wabbajack](https://github.com/wabbajack-tools/wabbajack/releases/latest/download/Wabbajack.exe) and place the `Wabbajack.exe` file inside the Wabbajack folder you created in Step 1.

3. Double-click the `Wabbajack.exe` file that is now inside your Wabbajack folder to set up the program.

>[!IMPORTANT]
>The list requires Wabbajack version **4.0.0.0 or later**. Installing the modlist on older versions of Wabbajack will result in issues.

#### Downloading and Installing Anvil

>[!CAUTION]
>**A legal copy of Skyrim Special Edition is required.** Pirated copies of the game will cause the installation to fail. GamePass versions do not work as well due to being incompatible with SKSE.

Downloading and installing Anvil can take a while depending on your internet connection, PC specs, and if you have Nexus Premium. Without Premium, you will need to manually click the **Slow Download** button for each mod.

To install Anvil, complete the following steps.

 1. Open Wabbajack and click `Browse Modlists`
 2. Pick the **Skyrim Special Edition** option from the game filter drop-down box (or use the search bar to find the modlist).
 3. Find the Anvil UI card and click the "Download and Install" button
 4. Set the `Installation Location` to a folder such as `C:\Anvil`.
    > - **DO NOT place it in Program Files, User folders (such as Desktop, Documents, Downloads, OneDrive, etc.), or in your Skyrim's Steam folder**
    > - The `Downloads Location` does not need to be on an SSD, but it makes installing faster. You can set this location to an HDD for the sake of saving space.
 5. Click the "Install" button to begin.
 6. Turn on your favorite show or a nice long video essay as Wabbajack does its thing. Alternatively read through this readme again.
 7. If the installation is successful, then rejoice and move onto [post installation](#post-installation-and-optional-setup). If the installation is unsuccessful, follow the tips below or the [discord server](https://discord.gg/4WwqfK5yHg) for support.

### Problems with installation

It is possible that you may encounter an error with Wabbajack when installing. Some common issues are listed below.

<Details>
<summary>I'm having trouble downloading Non-Nexus files or specific files!</summary>

Big files can fail to download due to connection issues or website issues. You can either run Wabbajack again or download the missing file manually. If you decide to manually download the file, make sure to place the file(s) inside the folder you set as the `Downloads Location`.

This issue can also occur with files sources from Google Drive, MEGA, Patreon, and other sites. Missing Manual Downloads are listed [here](#missing-manual-downloads).

</Details>

<Details>
<summary>Wabbajack couldn't find my game folder!</summary>

Either buy the game or re-read the [Pre-Installation](#pre-installation) section.  

</Details>  

<Details>
<summary>My antivirus reports a virus with the program or modlist!</summary>

Windows 10/11 may automatically quarantine a key file which is needed for Mod Organizer. You can fix this by [adding an exclusion for Mod Organizer in windows defender](#antivirus-exceptions).  

</Details>

<Details>
<summary>Unable to download "Data_ccbgssse037-curios": </summary>

Please make sure you are following the steps outlined in the [Installing Rare Curios Files](#installing-rare-curios-files) section

</Details>  

<Details>
<summary>Unable to download Skyrim_Default.ini:</summary>

This error means you failed to follow this Readme. Go back and follow the steps outlines in the [Changing the Game Language](#changing-the-game-language) section

</Details>  

<Details>
<summary>Sanity check error extracting file:</summary>

Wabbajack will sometimes have issues extracting files if they use special characters. If you encounter this issue in a Wabbajack log, please try the steps down below:

 1. Press `Win Key + R`.
 2. Type `intl.cpl` and hit `ENTER`.
 3. Navigate to *Administrative* and click `Change system locale...`.
 4. Change the *Current system locale:* to `English (United Kingdom)`.
 5. **Uncheck** `Beta: Use Unicode UTF-8 for worldwide language support`
 6. Click `OK`
 7. **Restart your PC** and rerun the Wabbajack installer.

</Details>  

<Details>
<summary>Wabbajack is crashing during the installation!</summary>

If you find yourself struggling to run Wabbajack without it crashing, freezing up, or blue-screening your PC, please try lowering Wabbajack's resource usage using these steps:

- Open the Wabbajack app
- Click the "Settings" button in the bottom-left corner of the Wabbajack window
- Under the "Performance" box, lower *each number for each category* to half of what it is set currently
  - *This will slow your download/install speed significantly. Feel free to decrease the values in increments to find a sweet spot.*
- Continue installation.

</Details>  

#### Missing Manual Downloads

Wabbajack frequently has trouble downloading mods hosted on sites other than Nexus. If you get an error such as **Missing Manual Downloads**, then read this section. You will need to manually download these files and place them in the `Downloads Location` that is made in the [Downloading and Installing Anvil](#downloading-and-installing-Anvil) section.

>[!WARNING]
> Make sure that you **DO NOT** unzip these files.

MEGA Files:

- [LM's Beast Teeth](https://mega.nz/folder/GJ0W2LxB#36be7O9y1oFUdrgFbLHfew/file/6FkwFYTA)
- [LM's EVG Hair Retex](https://mega.nz/folder/7VsT1LwT#sXtmEhgZH_JcRJlf0qIucQ/file/yJtmDZDR) (Grab both files in this MEGA folder)
- [High Poly Head - EFA - Eyebrow Make Fix](https://mega.nz/file/WZt0BDCL#JNUTn_5P2sEPuHm3znSdrrqN28tPnxvmVzeFOw67FAU)

Patreon Files:
- [zzjay's Horse Textures](https://www.patreon.com/file?h=65018177&i=10497594)

## Post-Installation and Optional Setup

### Stock Game

Anvil uses a Wabbajack feature called Stock Game to keep your Steam installation of Skyrim clean. All the files that you need to run the list are within your `Anvil/Stock Game` folder. Should Skyrim ever update again, this also ensures the modlist will not affected in anyway if you already have the modlist installed.

### Antivirus Exceptions

>[!WARNING]
>Antivirus programs are notorious for false flagging [MO2's Virtual File System](https://stepmodifications.org/wiki/Guide:Mod_Organizer/Advanced), which can and will cause crashes and other problems. Third-party AV programs such as BitDefender, Norton, and Webroot are especially aggressive, and you will most likely need to fully uninstall them in order to launch the game through MO2. It is 2024, Windows Defender and being smart online is more than adequate to protect yourself from malicious software.

If you use Windows Defender, it is advised that you set up an exception for the modlist.

<Details>
<summary>Setting up Windows Defender Exceptions:</summary>

 1. Press the Windows Key.
 2. Type "Windows Defender" in the search bar and select "Windows Security".
 3. Click on "Virus & threat protection" in the left pane.
 4. Click the "Manage settings" option under "Virus & threat protection settings".
 5. Scroll down to "Exclusions" and click "Add or remove exclusions".
 6. Windows Defender will prompt you with a run as administrator screen, just hit yes.
 7. Click the "Add an exclusion" button at the top and choose "Folder".
 8. Navigate to your Install folder for the list and click "Select Folder".
 9. **(OPTIONAL)** You can repeat these steps for the other executables:
    - ModOrganizer.exe (`[Path to Modlist]\ModOrganizer.exe`)
    - Nemesis Unlimited Behavior Engine.exe (`[Path to Modlist]\mods\Project New Reign - Nemesis Unlimited Behavior Engine\Nemesis_Engine\Nemesis Unlimited Behavior Engine.exe`)
    - Synthesis.exe (`[Path to Modlist]\tools\Synthesis\Synthesis.exe`)

</Details>  

### Post-Installation Issues and Troubleshooting

<Details>
<summary>Game is zoomed into the top left corner!</summary>

Windows Scaling can prevent games from displaying correctly, and will often result in the game appearing "zoomed in". To fix this, find the `SkyrimSE.exe` located in your `[Path to Modlist]\Stock Game` and follow the steps in the images below:

![](https://raw.githubusercontent.com/Oghma-Infinium/Apostasy/main/images/skyrim-scaling.png)

</Details>

<Details>
<summary>Form 43 Error in MO2. / A DLL plugin has failed to load correctly.</summary>

Your installation is corrupt. Rerun Wabbajack and make sure to tick the **Overwrite Installation** box. If the error persists after a reinstall, then delete the `[Path to Modlist]\mods` folder, and rerun Wabbajack again.

</Details>  

<Details>
<summary>Crashing on Startup</summary>

Send a message in the `#Anvil-Support` channel of our [discord](https://discord.gg/4WwqfK5yHg), including *all* relevant crash logs. There are several reasons why this might happen, and 99.9% of them are a corrupt installation.

</Details>  

</Details>

### Keyboard Keybinds

This section is going to be short, basic, and only go over the *additional modded keybinds*. All other controls, other than the ones listed below, are bound to vanilla keybinds.

Please refer the [this](https://ck.uesp.net/wiki/Input_Script) page for the DXScanCodes used by most mods if you'd like to change the binds for these mods **outside of the game**.

- [ReShade](https://reshade.me/): `Home` Key
    - ReShade Effects Toggle : `\` Key
- [Toggle UI](https://www.nexusmods.com/skyrimspecialedition/mods/112819): `F6` Key
    - Toggle Compass Only: `Right Shift + F6` Keys
    - Toggle Subtitles Only: `Right Ctrl + F6` Keys
- [Debug Menu](https://www.nexusmods.com/skyrimspecialedition/mods/136456): `F1` Key
- [Modex - A Mod Explorer Menu](https://www.nexusmods.com/skyrimspecialedition/mods/137877): `Delete` Key
- [Kreate](https://www.nexusmods.com/skyrimspecialedition/mods/83757): `Insert` Key
- [Community Shaders](https://www.nexusmods.com/skyrimspecialedition/mods/86492): `End` Key
- [True Directional Movement](https://www.nexusmods.com/skyrimspecialedition/mods/51614)'s Target Lock: `M3` button (Scroll Wheel button)

## Playing the Game

>[!WARNING]
>Before starting the list, read over the [Configuration](https://github.com/Oghma-Infinium/Anvil/blob/main/CONFIG.md) page.

 1. Head over to your modlist installation folder (e.g. `C:\Anvil`), locate an executable named `ModOrganizer.exe`, and launch it. Your first launch of Mod Organizer 2 may take several minutes due to GitHub repository downloads, so please be patient.

 2. Set up the [Configuration](https://github.com/Oghma-Infinium/Anvil/blob/main/CONFIG.md) page options if needed and set your CPU Affinity by following the instructions below. **DO NOT skip these instructions!**
    <Details>
    <summary>Setting CPU Affinity</summary>

    1. Click the `Puzzle Piece` button at the top of MO2 and select `Set CPU Affinity` and press `OK` on the pop-up box.

        ![](https://raw.githubusercontent.com/Oghma-Infinium/Vagabond/main/images/cpu%20affinity%20example.png)  
    2. That's it, it's really that simple. **Please, please, please** do this before launching the game and whenever you update the modlist.

    </Details>

 3. Click the "Play Anvil" Executable in MO2 to launch the game. The game may take several minutes to load on your first launch.

## Updating the modlist

Versioning for the list will adhere to the following format: `MAJOR.MINOR.PATCH`.

- `MAJOR`: Any release with a number change here will be considered a major update as at least 1 area of the list was massively overhauled. These updates with **NEVER** be save safe.
- `MINOR`: Any release with a number change here will be considered a minor update, these updates will **not** be save safe, unless otherwise specified.
- `PATCH`: Any release with a number change here will be considered a patch, these updates should be save safe and will be used primarily for bugfixes.
- In some rare cases, a fourth number will be used to designate a `HOTFIX`. These will only be utilized in cases where the list is recompiled with no other changes.

To update a modlist, follow these steps:
- Open the Wabbajack application
- Download the newest Wabbajack file for your modlist from the `Browse Lists` section by locating the modlist's UI card and clicking "Download & Install"
- Select the same `Installation Location` and `Downloads Location` folders you chose previously
- Click the "Install" button to begin installation

Changes to the modlist will be lost upon reinstall, so back up your modifications (such as INI tweaks or mod configs). If you want to keep mods you've added, prefix said mods with **[NoDelete]** to force Wabbajack to skip those files. 

>[!TIP]
>Saves can be continued across **Save-Safe** updates. Updates will be indicated whether or not they are **Save-Safe** on the [Changelog](https://github.com/Oghma-Infinium/Anvil/blob/main/CHANGELOG.md).

## Removing the Modlist

Simply delete the Anvil folder. Congratulations, you have uninstalled Anvil!

## Issues

If you encounter any bugs or issues while playing the list, the [Waking Dreams](https://discord.gg/4WwqfK5yHg) support server is preferred and will have the fastest turn around time for support.  Alternatively, you can leave an issue report via Github's [Issues](https://github.com/Oghma-Infinium/Anvil/issues) page, using the repository's template.

## Credits and Thanks

- *YOU* for reading this and checking out the modlist!
- [aljo](https://next.nexusmods.com/profile/aljoxo) for everything you've done and for being on this modding journey alongside me :3 (I also stole your readme nerd thanks for that too)
- [Althro](https://next.nexusmods.com/profile/Althro) for the original iteration of Anvil and his permission to alter it as I see fit (Really, thank you)
- [iAmMe27](https://ko-fi.com/iamme27) for general modding, documentation, and WJ assistance. Thanks friend :]
- The [Waking Dreams](https://discord.gg/4WwqfK5yHg) team for their time and effort playtesting, providing feedback, and support assistance <33
- [Ferroxius](https://next.nexusmods.com/profile/Ferroxius) for the original iteration of the Anvil MO2 Splash and Logo
- [Anvil MO2 Icon](https://www.flaticon.com/free-icons/anvil) created by Nikita on Flaticon
- [JustThatKing](https://next.nexusmods.com/profile/JustThatKing/about-me) for his visual academy that ended up jumpstarting my real deep dive into Skyrim's visual mods
- Bethesda Game Studios for Skyrim and the Creation Kit
- [ElminsterAU](https://www.patreon.com/ElminsterAU) and the xEdit team for SSEEdit
- [Noggog](https://www.nexusmods.com/skyrim/users/862590) for Mutagen and Synthesis
- [Halgari](https://www.nexusmods.com/skyrimspecialedition/users/17252164) and the WJ Team for the amazing platform that is Wabbajack
- [LivelyDismay](https://github.com/LivelyDismay) and [The Animonculory](https://github.com/The-Animonculory) for their modding guides
- [Sheson](https://ko-fi.com/sheson) for [DynDOLOD](https://dyndolod.info/) and associated tools
- All mod authors whose work is included, this list would not be possible without the greater modding community