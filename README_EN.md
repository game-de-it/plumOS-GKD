<img src="./asset/splash.png" width="640">  
<img src="./asset/IMG_0122.jpg" width="320">  

<img src="./asset/IMG_0123.jpg" width="320"> <img src="./asset/IMG_0125.jpg" width="320">  
<img src="./asset/IMG_0126.jpg" width="320"> <img src="./asset/IMG_0127.JPG" width="320">  
<img src="./asset/IMG_0128.JPG" width="320"> <img src="./asset/IMG_0129.JPG" width="320">  

[Latest Version 0.1](https://github.com/game-de-it/plumOS-GKD/releases) 

---
# Introduction
[Click here for the English version of the explanation](./README_EN.md)

plumOS-GKD is an OS customized based on StockOS.

## Download
[You can download the files from the "Releases page"](https://github.com/game-de-it/plumOS-GKD/releases).

## Changelog
[NEW] Version 0.1 has been released!

## Basic Features
- [pyxel v2.2.1](https://github.com/kitao/pyxel) is available.
- Emulationstation and gmenu2x are available as frontends.
  - To switch from ES to Gmenu2x, press the SELECT button and execute "GO LOVELYCHILD."
  - To switch from Gmenu2x to ES, execute the "ES" icon in the Setting section.
- The frontend is translated into English as much as possible.
- Portmaster is available.
- HDMI output is supported.
  - Please insert or remove the HDMI cable while the device is powered off.
- SD1 is formatted with EXT4, so you can transfer files via sftp over wifi or use SD2 formatted with fat32 (exFAT).
- SSH and sftp connection account:
  - Username: `root`, Password: `plumos`

## Known Issues
- USB-DAC and Bluetooth-AUDIO adapters are available but lack a switching mechanism.
- Pop noise may occur when Wifi is turned on, so it is recommended to keep it off when not needed.
- Due to library issues, the 64-bit and 32-bit versions of retroarch are not synchronized.

## Button Descriptions
<img src="./asset/sc01.png" width="320">  

## Retroarch Specifications
- Save files and state saves are created in the same folder as the rom file (modifiable).
- State save files are created in the same folder as the rom file (modifiable).
- RetroArch hotkeys:
  - ※Hotkey settings can be freely customized.

| Button Combo | Action | 
|:-----------|------------:|
| F1     |      Show Retroarch menu |
| SELECT+R       |        Save state |
| SELECT+L     |      Load state |
| SELECT+R2     |      Fast forward (2x speed) |
| SELECT+L2     |      Slow motion (1.5x speed) |
| SELECT+X     |      Screenshot (roms/screenshots) |
| SELECT+Y     |      Display FPS |

## OS Hotkeys
| Button Combo | Action | 
|:-----------|------------:|
| F2+Vol+       |        Increase screen brightness |
| F2+Vol-       |        Decrease screen brightness |

---
