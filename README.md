# OBS DVR System
OBS System for recreating Xbox Game DVR on Linux  
This system was originally made for [Devin](https://github.com/HiItsDevin), now it is getting uploaded to GitHub, mainly for archival purposes.

## Installation
**NOTE:** This guide assumes you are using Pop!\_OS 20.10 and GNOME 3.38, milage may vary :/
### Prerequisites
- OBS

### Steps to install
1. Download this repository, either by using a tool like `git` or `gh` or by downloading a ZIP file of the repository from [here](https://github.com/quinndoescode/obs-dvr/archive/refs/heads/trunk.zip).  
  a. For Git CLI: `git clone https://github.com/quinndoescode/obs-dvr.git`  
  b. For GitHub's CLI: `gh repo clone quinndoescode/obs-dvr`
2. Take the time to move the script labeled `obs-dvr-startup.sh` to a location you want it in. For this example, I put mine in `/home/quinn/obs-dvr/`
3. Open "Startup Applications" and add an entry with the options in here (obviously substituting the command path to the actual location you made in the previous step, then press Browse to find it.) by pressing the Add button on the right
![Visual instructions for steps 2 and 3](https://i.imgur.com/nYzpFZi.png)
4. Move the other file called `obs-dvr-backup.desktop` into `$HOME/.local/share/applications/`
![Visual instructions for step 4](https://i.imgur.com/Ygf4igN.png)
5. Open up OBS, go to Settings -> Output -> Check "Enable Replay Buffer" and change settings to taste
![Visual instructions for step 5](https://i.imgur.com/06Bi06W.png)
6. While still in Options, go to Hotkeys, scroll down to Replay Buffer -> Save Replay. Change Hotkey to what you want to press to be able to save last *n* seconds
![Visual instructions for step 6](https://i.imgur.com/0VpswAj.png)
7. Close OBS
8. Run "OBS DVR Launcher" from your application menu
![Visual instructions for step 8](https://i.imgur.com/46muXcM.png)

## Porting
It is very easy to port this to other distros/DMs. The entire thing revolves around the CLI one-liner `obs --startreplaybuffer --minimize-to-tray`

## FAQ
Q: I use Discord. I don't want streamer mode being enabled every time I restart my computer  
A: Disable it under User Settings -> Streamer Mode -> Uncheck "Automatically enable/disable"
