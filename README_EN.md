<img src="./asset/splash.png" width="640">  
  
<img src="./asset/IMG_0122.jpg" width="320"> <img src="./asset/IMG_0162.jpg" width="320">  
<img src="./asset/IMG_0123.jpg" width="320"> <img src="./asset/IMG_0125.jpg" width="320">  
<img src="./asset/IMG_0126.jpg" width="320"> <img src="./asset/IMG_0127.JPG" width="320">  
<img src="./asset/IMG_0128.JPG" width="320"> <img src="./asset/IMG_0129.JPG" width="320">  
<img src="./asset/IMG_0140.jpg" width="320">  

[Latest Version 0.3](https://github.com/game-de-it/plumOS-GKD/releases/tag/plumOS_GKD_v0.3) 

---
# Introduction
plumOS-GKD is a customized OS based on Bubble's StockOS (BBGV5.3 2024-10-15).  
The SD image for the mini PLUS includes partial applications of Bubble's StockOS.  
  - [Click here for detailed update information](https://github.com/game-de-it/plumOS-GKD/blob/main/about.txt)

## Supported Devices
- GKD Bubble
- GKD mini PLUS
- [Untested] GKD Mini PLUS Classic (metal casing with analog stick)

## Download
[You can download the SD image file from the "Releases" page](https://github.com/game-de-it/plumOS-GKD/releases).

## Update History
- [NEW!] picoarch is now available.
  - Refer to the specifications below for details.
- [NEW!] pyxel now supports online updates.
  - Ensure a WiFi connection and execute `pyxel_update` from the `tools` section in Emulationstation.
- [NEW!] A new Emulationstation theme, `es-theme-epic-cody-english`, has been added.
  - Thank you, tagiositaly.

## Basic Features
- [pyxel](https://github.com/kitao/pyxel) is supported.
- Equalizer functionality is available.
  - To permanently disable the equalizer, execute `Equalizer` in the `tools` section of Emulationstation.
- USB-DAC and Bluetooth AUDIO adapters are supported.
  - Connect USB devices while games are not running.
  - Confirmed compatible Bluetooth AUDIO dongles:
    - Creative BT-W2
    - GuliKit Route Air
- Frontends Emulationstation and gmenu2x are supported.
  - To switch from ES to Gmenu2x, press the SELECT button and execute "GO LOVELYCHILD."
  - To switch from Gmenu2x to ES, execute the "ES" icon in the Setting section.
- HDMI output is available (Bubble).
  - Plug or unplug the HDMI cable while the power is off.
- SD1 is formatted as EXT4, so transfer files via WiFi (SFTP) or format SD2 as FAT32 (exFAT).
- SSH and SFTP account:
  - Username: `root`, Password: `plumos`.

## Known Issues
- Turning on WiFi may cause popping noise; keep it off when not in use.
- Some games in portmaster do not run.
- Scraping functionality is unavailable.

## CPU and GPU Performance
- By default, the CPU frequency scales automatically between 400MHz and 1992MHz based on load. Explicitly setting max performance may stabilize certain games:
  - To set max performance for specific emulators:
    - In the ROM selection screen, press SELECT and set `CPU SCALING GOVERNOR` to `PERFORMANCE` and `GPU PERFORMANCE PROFILE` to `BEST PERFORMANCE` under `ADVANCED SYSTEM OPTIONS.`
  - To set max performance for specific ROMs:
    - Highlight the ROM, press X, and set `CPU SCALING GOVERNOR` to `PERFORMANCE` and `GPU PERFORMANCE PROFILE` to `BEST PERFORMANCE` under `ADVANCED GAME OPTIONS.`
  - To set max performance globally:
    - Press START, go to `SYSTEM SETTINGS`, and set `DEFAULT SCALING GOVERNOR` to `PERFORMANCE` and `GPU PERFORMANCE PROFILE` to `BEST PERFORMANCE.`

## Button Descriptions
<img src="./asset/sc01.png" width="320">  

## picoarch Specifications
- How to use picoarch:
  - Emulationstation:
    - In the ROM selection screen, press SELECT and choose an emulator from `ADVANCED SYSTEM OPTIONS.`  
      <img src="https://github.com/game-de-it/plumOS-GKD/blob/main/asset/IMG_0370.jpg" width="320">
  - LOVELYCHILD (gmenu2x):
    - Run the emulator from the `pico` section.  
      <img src="https://github.com/game-de-it/plumOS-GKD/blob/main/asset/IMG_0371.jpg" width="320">  
- Location of picoarch save data:
  - Save data is stored in the `/storage/.config/.picoarch/data` directory.
- Supported libretro cores:

| libretro Core |  |
|:-------|-------:|
|quicknes|beetle_wswan|
|mgba|snes9x2010|
|picodrive|pokemini|
|smsplus-gx|pcsx_rearmed|
|beetle_ngp|beetle-pce-fast|
|gambatte||

- picoarch Hotkeys:
  - Fast forward is not available for some cores

| Button Combo | Action | 
|:-----------|------------:|
| SELECT+START     |      Open menu |
| SELECT+R       |        Save state |
| SELECT+L     |      Load state |
| SELECT+R2     |      Fast forward |
| SELECT+L2     |      Display FPS |

- picoarch Resolutions:

| Name | Resolution | 
|:-----------|------------:|
| picoarch_LD     |  320x240 |
| picoarch_HD       |  640x480 |

## Retroarch Specifications
- Save files and state saves are created in the same folder as the ROM file (configurable).
- RetroArch Hotkeys:
  - *Hotkey settings are freely configurable.*  

| Button Combo | Action | 
|:-----------|------------:|
| F1     |      Open Retroarch menu |
| SELECT+R       |        Save state |
| SELECT+L     |      Load state |
| SELECT+R2     |      Fast forward (2x) |
| SELECT+L2     |      Slow motion (1.5x) |
| SELECT+X     |      Take a screenshot (roms/screenshots) |
| SELECT+Y     |      Display FPS |

## OS Hotkeys
| Button Combo | Action | 
|:-----------|------------:|
| F2+Vol+       |        Increase screen brightness |
| F2+Vol-       |        Decrease screen brightness |

## retrorun Specifications
- retrorun Hotkeys:
<img src="./asset/setting.png" width="320"> 

## Save Data Locations for Each Emulator
Use this as a reference for backing up save data:
| Emulator | DIR | 
|:-----------|------------:|
| drastic       |        /storage/.config/drastic |
| ppsspp       |         /storage/.config/ppsspp |
| retroarch    |       Within each ROM directory |
| picoarch | /storage/.config/.picoarch/data |
| Other Emulators      |       /storage/roms/savestates |

---
