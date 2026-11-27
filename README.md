<div align="center">

# Galaxy on Fire 2 FULL HD — Android 64-bit

**Galaxy on Fire 2 FHD running natively on modern 64-bit Android devices.**

[![Discord](https://dcbadge.limes.pink/api/server/N4F4aMQ6XP?style=flat)](https://discord.com/invite/N4F4aMQ6XP)
[![X (Twitter)](https://img.shields.io/twitter/follow/KiritoJPK?style=flat&logo=x)](https://twitter.com/KiritoJPK)
[![Downloads](https://img.shields.io/github/downloads/KiritoJPK/GOF2-FHD-Android-64-bit/total)](https://github.com/KiritoJPK/GOF2-FHD-Android-64-bit/releases)
[![Release](https://img.shields.io/github/release/KiritoJPK/GOF2-FHD-Android-64-bit)](https://github.com/KiritoJPK/GOF2-FHD-Android-64-bit/releases/latest)
[![4PDA](https://img.shields.io/badge/-4PDA_GOF2-0854C1)](https://4pda.to/forum/index.php?showtopic=483666)

**[⬇ Download the latest release](https://github.com/KiritoJPK/GOF2-FHD-Android-64-bit/releases/latest)**

If you liked the project and would like to help me keep it going with a donation, I would be very grateful. [![Ko-fi](https://img.shields.io/badge/Ko--fi-FF5E5B?logo=ko-fi&logoColor=white)](https://ko-fi.com/kiritojpk)

</div>

## About

Galaxy on Fire 2 FHD for Android is a fan-made retexturing and enhancement project. It uses the original assets from the macOS, Windows and iPhone versions to bring the Android game closer to them, with interface changes and no FPS limit.

The original Android game only exists as 32-bit code, and many recent phones can no longer run 32-bit apps. This version runs that same game on 64-bit devices through a bridge built on [Dynarmic](https://github.com/azahar-emu/dynarmic), which translates the game's ARM32 code to ARM64 while it runs. It continues the [32-bit project](https://github.com/KiritoJPK/GOF2-FHD-Android), which no longer receives updates.

## Features

### Graphics
- Full HD textures from the PC and Mac versions, with no cap on the game resolution
- Bloom and Motion blur options, as on iOS
- Hangar robots and Vossk bar robots from the first version of the game

### Controls
- **Gamepad:** steering, weapons, boost, docking and the HUD buttons in flight, with an on-screen cursor in the menus
- **Keyboard and mouse:** the macOS key layout, strafing with A/D, mouse steering in flight, and the mouse wheel in menus and in the hangar
- Better accelerometer, smoother star map dragging, and a back button that no longer blocks the interface

### Gameplay
- **Supernova Challenge**, the iOS score mode
- **Easy and Hard difficulty** restored
- Game over screen, skip button in the prologue, and the About page moved to Options
- Credit store removed; credit purchases give nothing
- Screenshots saved to the gallery and to `GOF2/pictures`

### Performance and audio
- Faster emulation: direct calls, read-only game code, and rendering that has priority over the audio
- Game time aligned to the screen for smoother motion
- Shorter audio buffers, and a fix for the freeze in the Valkyrie hangar

### Settings menu
The menu that opens before the game lets you choose:
- **Frame rate:** 30 FPS, 60 FPS or VSync
- **Economy:** Default, Android or Custom (see below)
- **Screen scale:** from 50% to 150%

## Requirements

- A device with a **64-bit ARM** processor (arm64-v8a)
- **Android 8.0** or newer

## Installation

The game data can be inside the APK or in a separate OBB file.

- **APK with the data:** just install the APK.
- **APK + OBB:** install the APK, then copy the `main.*.obb` file to
  `Android/obb/net.fishlabs.gof2hdallandroid2012/`

When the game audio inside the OBB is compressed, the first start extracts it once while a message says *"Extracting the game audio, please wait"*. Later starts skip this step.

## Economy

The game includes two types of economy:

- **Default economy:** the prices of the macOS, Windows and iPhone versions.
- **Android economy:** much higher costs for some equipment and for the resources needed by blueprints.

There is also a **Custom** option for modders: any `.bin` file placed in `GOF2/mods/bin` (in the root of the device storage) replaces the game's own file. Files that are not there come from the default economy. Custom needs the "All files access" permission, which the menu asks for.

> [!WARNING]
> Only load saves made with the economy that is currently selected. A save from another economy will be full of bugs.

## Building the bridge

The bridge builds on Windows with `build_arm64.bat`. It needs:

- Android SDK with **NDK 27.2.12479018** and **CMake 3.22.1**
- **Git** (CMake downloads the pinned Dynarmic source)

The result is `build_arm64/libgof2_arm64_bridge.so`. Every change on top of the original game can be turned on or off in `src/bridge_features.h`, and `CHANGELOG.md` describes each one.

## Reporting bugs

Found a bug? Open an [issue](https://github.com/KiritoJPK/GOF2-FHD-Android-64-bit/issues/new) or tell us on [Discord](https://discord.com/invite/N4F4aMQ6XP). Please check the [open issues](https://github.com/KiritoJPK/GOF2-FHD-Android-64-bit/issues) first, in case it was already reported.

To help us fix it, include:

- **Device** model and **Android version**
- **Game version** (the release you installed) and whether you use the APK alone or APK + OBB
- **What happened** and **what you expected**
- **Where** it happened (station, system, mission or menu) and the **steps** to make it happen again
- Whether it happens **every time** or only sometimes
- A **screenshot or video**, if you can

If the game crashes or freezes, also say what you were doing right before it.

## Screenshots

![Screenshot](https://github.com/user-attachments/assets/a5b8a78d-f85f-4caf-82ef-aee520710c75)
![Screenshot](https://github.com/user-attachments/assets/a2a45302-811d-4f49-88f1-85f0400afca1)

## Credits

- **Opera-Fan**, for the source code of the bridge
- **[Dynarmic](https://github.com/azahar-emu/dynarmic)**, the ARM translator the bridge is built on
- Many of the included modifications came from 4PDA community projects created by **Dhаmpir, atang, Droid378, leningroz, Ворон, Ravenstal, meng00701, Bibifire, Pb-207** and **KrYcHokE**. Thank you!

---

<sub>This is a non-commercial fan project and is not affiliated with FISHLABS or Deep Silver. Galaxy on Fire 2 and its assets belong to their respective owners.</sub>
