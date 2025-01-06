-=(TimePilot84_Senhor notes)=-

Tested: Working Video 720p, 1080p & Sound

Dev notes: Barely seen pixel artifacts on title screen. Gameplay is not affected
___
# Time Pilot '84 for [MiSTer](https://github.com/MiSTer-devel/Main_MiSTer/wiki)
An FPGA implementation of Time Pilot '84 by Ace, ElectronAsh, Enforcer, loloC2C and Kitrinx

## Features
- Timing-accurate logic model made to match the original as closely as possible
- Keyboard and joystick controls
- Greg Miller's cycle-accurate MC6809E CPU core with modifications by Sorgelig and bugfixes by Arnim Laeuger and Jotego
- T80s CPU by Daniel Wallner with fixes by MikeJ, Sorgelig, and others
- SN76489 sound core by Arnim Laeuger with fixes by Ace and Enforcer
- Fully-tuned audio filters (selectable within the core) including the PCB's switchable low-pass filters
- Option for normalized video timings to use with picky HDTVs and monitors (underclocks the game by ~1%)

## Installation
Place `*.rbf` into the "_Arcade/cores" folder on your SD card.  Then, place `*.mra` into the "_Arcade" folder and ROM files from MAME into "games/mame".
For authentic audio filtering, place the `filters_audio` folder onto the root of the SD card and select one of the two provided filter presets from within the core.
`TP84 Light LPF` simulates the PCB's audio filtering when volume-matched to the core's volume while `TP84 Heavy LPF` simulates the PCB's audio filtering when set as loud as possible before clipping.

### ****ATTENTION****
ROMs are not included. In order to use this arcade core, you must provide the correct ROMs.

To simplify the process, .mra files are provided in the releases folder that specify the required ROMs along with their checksums.  The ROM's .zip filename refers to the corresponding file in the M.A.M.E. project.

Please refer to https://github.com/MiSTer-devel/Main_MiSTer/wiki/Arcade-Roms for information on how to setup and use the environment.

Quick reference for folders and file placement:

/_Arcade/<game name>.mra
/_Arcade/cores/<game rbf>.rbf
/games/mame/<mame rom>.zip
/games/hbmame/<hbmame rom>.zip

## Controls
### Keyboard
| Key | Function |
| --- | --- |
| 1 | 1-Player Start |
| 2 | 2-Player Start |
| 5, 6 | Coin |
| 9 | Service Credit |
| Arrow keys | Movement |
| CTRL | Shot |
| ALT | Missile |

## Known Issues
1) Resolution is incorrectly reported as 253x224

