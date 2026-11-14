![header](header.png?raw=true)

# Sonic Mania Decompilation Plus

Fork of [RSDKModding](https://github.com/RSDKModding/)'s [Sonic Mania Decompilation](https://github.com/RSDKModding/Sonic-Mania-Decompilation) that ports features I introduced in my [SonicWebMania](https://github.com/pustal/SonicWebMania) project.

It uses [RSDK v5U Decompilation Plus](https://github.com/pustal/RSDKv5-Decompilation-Plus), my own fork of [RSDKModding](https://github.com/RSDKModding/)'s [RSDK v5U Decompilation](https://github.com/RSDKModding/RSDKv5-Decompilation).

## **SUPPORT THE OFFICIAL RELEASE OF SONIC MANIA (PLUS)**
+ Without assets from the official releases, this decompilation will not run.

+ You can get the official release of Sonic Mania (Plus) from:
  * Windows
    * [Via Steam](https://store.steampowered.com/app/584400/Sonic_Mania/)
    * [Via The Epic Games Store](https://www.epicgames.com/store/en-US/p/sonic-mania)
  * [Switch, via the eShop](https://www.nintendo.com/games/detail/sonic-mania-switch/)
  * [PS4, via the Store](https://store.playstation.com/en-us/product/UP0177-CUSA07023_00-SONICMANIA000000)
  * [Xbox One, via the Store](https://www.xbox.com/en-US/games/store/sonic-mania/BXH46NQT9W4Q/0001)

Even if your platform isn't supported by the above official releases, you **must** buy it for the assets. The Netflix Games version is NOT supported.

## **DO NOT USE THIS DECOMPILATION PROJECT AS A MEANS TO PIRATE SONIC MANIA (PLUS)**
We do not condone using this project as a means for piracy in any form. This project was made with love and care for the source material and was created for purely educational purposes, and would not exist without the work of Sega, Headcannon, and Evening Star.

If you want to transfer your save from the official PC versions, you can just copy your savedata into the folder containing the decompilation!

# Plus:

## Retro games next to Sonic Mania
This fork builds the [RSDKv5-Decompilation-Plus](https://github.com/pustal/RSDKv5-Decompilation-Plus) engine, which plays **Sonic the Hedgehog, Sonic 2 and Sonic CD** next to Sonic Mania from your own data packs (Sonic Origins' and/or the earlier releases'), with:
* the **Plus menu** (press Select, Tab on a keyboard): switch games, achievements, settings;
* the **Plus DLC off by default**, as the decompilation's licence asks of every build: Sonic Mania Plus (Encore mode, Mighty, Ray...) and Sonic Origins Plus (Amy, and Knuckles in Sonic CD). If you own them, turn them on in the Plus menu's Settings (**Plus DLC**, press OK twice; the game restarts) or with `plusDLC=y` under `[Game]` in `Settings.ini`;
* **save slots and Sonic Origins' modes** (Anniversary, Classic, Mirror, Boss Rush) and coins;
* **Sonic Mania's music and sounds** filling what the retro packs lack (the Origins packs have no audio), and optionally **Mania's remixes** of Green Hill, Chemical Plant, Oil Ocean, Stardust Speedway and Metallic Madness even over the earlier releases' originals;
* **touch controls on Android**: the PAD button at the top right shows a pad and buttons over the game, with an adjustable opacity;
* **on Windows, a resizable window** (move, resize, maximise; the picture follows, and it starts at a size that fits the screen) and **PlayStation, Nintendo and other controllers** next to Xbox ones, with their own button prompts.

Put the packs in a `retro` folder next to `Data.rsdk` (`sonic1-origins.rsdk`, `sonic1-classic.rsdk`, ...): see the engine's README for the names and details. No game data is included.

The RSDK files should be placed and renamed as following:

```
Data.rsk
retro/
| sonic1-classic.rsdk
| sonic1-origins.rsdk
| sonic2-classic.rsdk
| sonic2-origins.rsdk
| soniccd-classic.rsdk
| soniccd-origins.rsdk
```
Sonic Mania Decompilation Plus also support converting the sound files directly from Sonic Origins for its version of the retro games. The original sound files can be sourced from Sonic Origins's installation folder in `image/x64/raw/sound` and should be places in `retro/origins` and can be converted in the overlay menu (`tab` / `select button` / `back button` -> `Settings` -> `Convert Sonic Origins audio`).

Audio files have the following contents:

| File | Sound contents |
|---|---|
| `HITE_sfx.acb` | All three retro games |
| `STH1_sfx.acb` | Sonic 1 (and three of Sonic 2's jingles) |
| `STH1_music.acb` | Sonic 1 (and three of Sonic 2's jingles) |
| `STH1_music.awb` | Sonic 1 (and three of Sonic 2's jingles) |
| `STH2_sfx.acb` | Sonic 2 |
| `STH2_music.acb` | Sonic 2 |
| `STH2_music.awb` | Sonic 2 |
| `SCD_sfx.acb` | Sonic CD |
| `SCD_music.acb` | Sonic CD |
| `SCD_music.awb` | Sonic CD |

As well as supporting the following video files from Sonic Origins with the following contents:

| File | Video contents |
|---|---|
| `sonicteam_logo.usm` |	all three games (the Sonic Team logo) |
| `hite_sonic1_intro.usm` |	Sonic 1 |
| `hite_sonic1_outro.usm` |	Sonic 1 |
| `hite_sonic2_intro.usm` |	Sonic 2 |
| `hite_sonic2_outro.usm` |	Sonic 2 |
| `soniccd_op.usm` |	Sonic CD |
| `cd_ed_good.usm` |	Sonic CD |
| `cd_ed_bad.usm` |	Sonic CD |
| `hite_soniccd_intro.usm` | Sonic CD |
| `hite_soniccd_outro.usm` | Sonic CD |

Remaining audio and vídeo files from Sonic Origins are currently unused by this project.

To be clear, with the vídeo and sound files, the structure is as follows:

```
Data.rsk
retro/
| sonic1-classic.rsdk
| sonic1-origins.rsdk
| sonic2-classic.rsdk
| sonic2-origins.rsdk
| soniccd-classic.rsdk
| soniccd-origins.rsdk
| origins/
| | HITE_sfx.acb
| | STH1_sfx.acb
| | STH1_music.acb
| | STH1_music.awb
| | STH2_sfx.acb
| | STH2_music.acb
| | STH2_music.awb
| | SCD_sfx.acb
| | SCD_music.acb
| | SCD_music.awb
| | sonicteam_logo.usm
| | hite_sonic1_intro.usm
| | hite_sonic1_outro.usm
| | hite_sonic2_intro.usm
| | hite_sonic2_outro.usm
| | soniccd_op.usm
| | cd_ed_good.usm
| | cd_ed_bad.usm
| | hite_soniccd_intro.usm
| | hite_soniccd_outro.usm
```

The game RSDK files can can be sourced as following:

| Pack | Where it comes from |
|---|---|
| Sonic Origins | `Sonic1u.rsdk`, `Sonic2u.rsdk`, `SonicCDu.rsdk` from the game's install folder (`retro`) |
| Earlier release | Sonic 1 and 2 (2013): `Data.rsdk` (Android: `Data.rsdk.xmf` in the APK, you can decompress it with tools like 7zip). Sonic CD (2011): `Data.rsdk.xmf` from the mobile app's APK, or `Data.rsdk` from Steam |

How each game plays depends on what you upload:

| Packs | Result |
|---|---|
| Origins only | The Origins game. Origins keeps its audio outside these packs, so without Sonic Mania or the audio packs, it is silent; with Sonic Mania aline, see **Sound from Sonic Mania** below |
| Origins + earlier release | The Origins game, with the earlier release's music and sound effects. The sounds Origins added (Drop Dash, Knuckles' and Amy's moves) come from Sonic Mania when it is installed, otherwise they are silent if Sonic Origins audio packs aren't present and converted. If they are, they are used instead of the earlier releases |
| Earlier release only | Sonic 1 and 2: that release. Sonic CD: the mobile pack is the 2011 game, with its own menus, save slots and Time Attack. The Steam pack can't be played alone (its scripts are stored the way the PC build named them, which the engine doesn't load); it only adds sound to the Origins game |

- **Sound from Sonic Mania.** With Sonic Mania's `Data.rsdk` installed, whatever music or
  sound effect a retro game's packs lack comes from Mania's pack (on by default; a
  checkbox on the page turns it off). The game's own packs always win.
  - Sound effects: Mania's file of the same name (jumps, rings, springs, the Drop Dash,
    Knuckles' glide and climb...), or its nearest one; Amy's hammer uses Mania's hits
    and jumps.
  - Music: the zones and jingles Mania remixed, with Mania's loop points: Green Hill,
    Chemical Plant and Oil Ocean (Mania's act 1 remix in act 1, its act 2 remix from
    act 2 on), Stardust Speedway and Metallic Madness (by time period), plus
    invincibility, speed shoes, act clear, boss, drowning, game over and Super.
  - **Sonic Mania remixes** (off by default): those zones play Mania's remix even when the
    earlier release's pack has the original, and their speed shoes play Mania's jingle.
  - **Similar Mania music** (off by default): zones Mania has no version of get a Mania track
    of similar feel, such as Emerald Hill with Green Hill, Casino Night with Studiopolis,
    Aquatic Ruin and Tidal Tempest with Hydrocity, Mystic Cave and Quartz Quadrant with
    Lava Reef. The title, special stage and credits use Mania's own.

  A Mania track that only shares a name with a retro one (its title screen, credits) is
  not played unless similar music is on.
- **Save slots.** Starting Sonic 1 or 2 opens a save screen: play without saving, or
  pick one of four slots to continue (zone, character, lives and emeralds are shown),
  start a new game, or delete it (press OK twice). New games then choose the character:
  Sonic, Tails, Knuckles, Sonic & Tails, and with the Origins packs Knuckles & Tails,
  Amy and Amy & Tails. The games save their own progress as you play (at the end of
  each act), as the 2013 releases did. The 2013 packs' title screen cannot start a game
  by itself (those releases used native menus), so for them the save screen opens when
  the title would start its demo. Sonic CD goes to its own 2011 menu instead: its save
  slots, Time Attack and extras. The mobile pack's menus work with the buttons, and also
  take a touch (a mouse click on a computer).
- **Sonic Origins' modes.** With the Origins packs the save screen starts with a mode:
  - **Anniversary**: extra lives become coins, no time limit;
  - **Classic**: lives and the 10-minute time limit (and, in Sonic 1, no spin dash);
  - **Mirror**: Anniversary rules with the stages mirrored and left/right swapped (the HUD
    and title cards stay readable);
  - **Boss Rush** (experimental): the bosses one after another, without saving; a defeat
    retries the fight. Sonic 1's Boss Rush stages are whole acts, so, as Origins does,
    the port starts you at the act's last checkpoint, next to the boss. Moving on to the
    next boss is untested.

  Coins are kept in `RetroCoins.ini` in the app's data folder, shared by the three games as
  in Origins. Missions, the Museum and Story mode are part of Origins' own program, not of
  its packs, so they are not available.
- **Achievements.** Each game has its own twelve achievements (those of the 2013 and
  2011 releases, which the Origins packs share), unlocked as you play: a notice shows
  each one, the Back menu's Achievements page lists them, and they are kept in the game's
  `Achievements.bin`. Sonic CD's own menu entry opens the same list (its Leaderboards
  entry needs an online service, so it only says so).
- Sonic 3 & Knuckles from Origins cannot be played: its game code lives in the Origins
  program, not in its pack.

You can switch the current game playing in the 

## Extra features menu:
Access the extra features menu at any time, by pressing the tab key or the "select" button.

# Additional Tweaks
* Added a built-in mod loader and API calls to enable a much smoother modding experience.
* Added support for targeting RSDKv5U rather than standalone RSDKv5
* Added support for building almost all released versions of the game. Including: 1.00 (Console initial release), 1.03 (PC initial release) & 1.06 (Plus update)

# How to Build

This project uses [CMake](https://cmake.org/), a versatile building system that supports many different compilers and platforms. You can download CMake [here](https://cmake.org/download/). **(Make sure to enable the feature to add CMake to the system PATH during the installation if you're on Windows!)**

## Get the source code

**DO NOT** download the source code ZIP archive from GitHub, as they do not include the submodules required to build the decompilation.

Instead, you will need to clone the repository using Git, which you can get [here](https://git-scm.com/downloads).

Clone the repo **recursively**, using:
`git clone --recursive https://github.com/pustal/Sonic-Mania-Decompilation-Plus`

If you've already cloned the repo, run this command inside of the repository:
```git submodule update --init --recursive```

## Getting dependencies

This repo includes everything you need for Sonic Mania + RSDKv5(U). If you wish to compile only Sonic Mania, you can skip to the [compilation steps below](#compiling) and compile with the `WITH_RSDK` flag disabled.

### Windows
To handle dependencies, you'll need to install [Visual Studio Community](https://visualstudio.microsoft.com/downloads/) (make sure to install the `Desktop development with C++` package during the installation) and [vcpkg](https://learn.microsoft.com/en-us/vcpkg/get_started/get-started?pivots=shell-cmd#1---set-up-vcpkg) (You only need to follow `1 - Set up vcpkg`).

After installing those, run the following in Command Prompt (make sure to replace `[vcpkg root]` with the path to the vcpkg installation!):
- `[vcpkg root]/vcpkg.exe install libtheora libogg glew glfw3 sdl2 --triplet=x64-windows-static` (If you're compiling a 32-bit build, replace `x64-windows-static` with `x86-windows-static`.)

Finally, follow the [compilation steps below](#compiling) using `-DCMAKE_TOOLCHAIN_FILE=[vcpkg root]/scripts/buildsystems/vcpkg.cmake -DVCPKG_TARGET_TRIPLET=x64-windows-static` as arguments for `cmake -B build`.
  - Make sure to replace `[vcpkg root]` with the path to the vcpkg installation!
  - If you're compiling a 32-bit build, replace `x64-windows-static` with `x86-windows-static`.

### Linux
Install the following dependencies: then follow the [compilation steps below](#compiling):
- **pacman (Arch):** `sudo pacman -S base-devel cmake glew glfw libtheora`
- **apt (Debian/Ubuntu):** `sudo apt install build-essential cmake libglew-dev libglfw3-dev libtheora-dev`
- **rpm (Fedora):** `sudo dnf install make cmake gcc glew-devel glfw-devel libtheora-devel zlib-devel`
- **xbps (Void):** `sudo xbps-install make cmake gcc pkg-config glew-devel glfw-devel libtheora-devel zlib-devel`
- Your favorite package manager here, [make a pull request](https://github.com/RSDKModding/Sonic-Mania-Decompilation/fork) (also update [RSDKv5U](https://github.com/RSDKModding/RSDKv5-Decompilation)!)

#### (make sure to [install GL shaders!](#q-why-arent-videosfilters-working-while-using-gl))

### MacOS
Check the [MacOS dependencies README on RSDK v5U Decompilation Plus](https://github.com/pustal/RSDKv5-Decompilation-Plus/tree/master/dependencies/mac). You'll need `Game.dylib` compiled by this project to accompany the app (see below).

### Switch
[Setup devKitPro](https://devkitpro.org/wiki/Getting_Started), then run the following:
- `(dkp-)pacman -Syuu switch-dev switch-libogg switch-libtheora switch-sdl2 switch-glad`

Finally, follow the [compilation steps below](#compiling) using `-DCMAKE_TOOLCHAIN_FILE=/opt/devkitpro/cmake/Switch.cmake` as arguments for `cmake -B build`.

#### (make sure to [install GL shaders!](#q-why-arent-videosfilters-working-while-using-gl))

### Wii, Wii U and PlayStation Vita
These link the game into the engine (`-DGAME_STATIC=ON`). Install the toolchain and libraries listed in [RSDKv5 Decompilation Plus's README](https://github.com/pustal/RSDKv5-Decompilation-Plus#wii), then follow the [compilation steps below](#compiling) with these arguments for `cmake -B build`:
- **Wii:** `-DCMAKE_TOOLCHAIN_FILE=/opt/devkitpro/cmake/Wii.cmake -DPLATFORM=NintendoWii -DGAME_STATIC=ON` (gives `RetroEngine.dol`, the Homebrew Channel's `boot.dol`)
- **Wii U:** `-DCMAKE_TOOLCHAIN_FILE=/opt/devkitpro/cmake/WiiU.cmake -DPLATFORM=NintendoWiiU -DGAME_STATIC=ON` (gives `RetroEngine.wuhb`)
- **Vita:** `-DCMAKE_TOOLCHAIN_FILE=$VITASDK/share/vita.toolchain.cmake -DPLATFORM=PlayStationVita -DGAME_STATIC=ON` (gives `RSDKv5U.vpk`)

### Android
**Ensure you clone the repo recursively,** then follow the RSDK build instructions [here.](https://github.com/RSDKModding/RSDKv5-Decompilation/blob/master/dependencies/android/README.md)

## Compiling

Compiling is as simple as typing the following in the root repository directory:
```
cmake -B build
cmake --build build --config release
```

The resulting build for Mania will be located somewhere in `build/` depending on your system.
If building with RSDKv5(U), the resulting Mania and RSDK executable will likely be in `build/dependencies/RSDKv5/`.

The following cmake arguments are available when compiling:
- Use these by adding `-D[flag-name]=[value]` to the end of the `cmake -B build` command. For example, to build with `RETRO_DISABLE_PLUS` set to on, add `-DRETRO_DISABLE_PLUS=on` to the command.

### RSDKv5 flags
- `RETRO_REVISION`: What revision to compile for. Takes an integer, defaults to `3` (RSDKv5U).
- `RETRO_DISABLE_PLUS`: Forces the Plus DLC off, with no way to turn it on. Takes a boolean (on/off), defaults to `off`. Without it the DLC is still off by default and only the player turns it on (Settings.ini `Game:plusDLC`, or the Plus menu), as the licence allows.
- `RETRO_MOD_LOADER`: Enables or disables the mod loader. Takes a boolean, defaults to `on`.
- `RETRO_MOD_LOADER_VER`: Manually sets the mod loader version. Takes an integer, defaults to the current latest version.
- `RETRO_PLUS`: Enables the engine's Plus features (retro games, the Plus menu, Sonic Mania's audio for the retro games). Not the Sonic Mania Plus DLC (see `RETRO_DISABLE_PLUS`). Takes a boolean, defaults to `on`.
- `RETRO_WIN_SDL2_INPUT`: Windows, DirectX 9 and 11: reads PlayStation, Nintendo and other non-XInput controllers through SDL2, when SDL2 is found (`vcpkg install sdl2`). Takes a boolean, defaults to `on`.
- `RETRO_SUBSYSTEM`: *Only change this if you know what you're doing.* Changes the subsystem that RSDKv5 will be built for. Defaults to the most standard subsystem for the platform.

### Sonic Mania flags
- `WITH_RSDK`: Whether or not RSDKv5 is built alongside Sonic Mania. Takes a boolean, defaults to `on`.
  - `GAME_STATIC`: Whether or not to build Sonic Mania into the resulting RSDKv5 executable. Takes a boolean, defaults change depending on the system.
- `MANIA_FIRST_RELEASE`: Whether or not to build the first console release of Sonic Mania. Takes a boolean, defaults to `off`.
- `MANIA_PRE_PLUS`: Whether or not to build a pre-plus version of Sonic Mania. Takes a boolean, defaults to `off`.
- `GAME_INCLUDE_EDITOR`: Whether or not to include functions for use in certain RSDKv5 scene editors. Takes a boolean, defaults to `on`.
- `GAME_VERSION`: Which release version of Sonic Mania to target for. Takes an integer, defaults to `3` when `MANIA_PRE_PLUS` is enabled, and `6` otherwise (last steam release).

### Windows
```
:: (cmake --build build --config Release --target clean)
cmake -B build -DCMAKE_TOOLCHAIN_FILE=<vcpkg dir>/scripts/buildsystems/vcpkg.cmake -DVCPKG_TARGET_TRIPLET=<triplet option> :: (example: `cmake -B build -DCMAKE_TOOLCHAIN_FILE=C:/vcpkg/scripts/buildsystems/vcpkg.cmake -DVCPKG_TARGET_TRIPLET=x64-windows-static`)
cmake --build build --config Release
```

### MacOS
Open `Sonic-Mania-Decompilation-Plus/SonicMania.xcodeproj`.
Choose the SonicMania scheme, set it to Release, then Clean Build Folder and Build. It'll generate `Game.dylib` to accompany the RSDKv5U app generated in the dependencies section.

### Other Platforms
The only directly supported platforms are those listed above. Since Mania is very easy to build, requiring no additional dependencies, virtually any platform that can run RSDKv5 can compile Mania easily.

Check my [SonicWebMania](https://github.com/pustal/SonicWebMania) project for a WebOS port.

However, there are a multitude of ports listed in the **[RSDKv5 repository.](https://github.com/RSDKModding/RSDKv5-Decompilation)**. Note that these are ports of the original RSDKv5 and Sonic Mania Decompilations and not this Plus version (the Wii, Wii U and Vita ports are part of this one, see above).

# FAQ
### Q: Why aren't videos/filters working while using GL?
A: There's a mod for it that you have to make. Refer to the following directions:

Create the following directory structure inside your mods directory:
```
GLShaders/
| Data/
| | ...
| mod.ini
```

Inside `mods/GLShaders/Data/`, copy the `RSDKv5/Shaders` directory, and inside the `mod.ini`, paste this:
```
Name=GLShaders
Description=GL3 shaders
Author=Ducky
Version=1.0.0
TargetVersion=5
```
