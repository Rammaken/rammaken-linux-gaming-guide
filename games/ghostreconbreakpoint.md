# <img src="https://cdn2.steamgriddb.com/icon_thumb/85051e0cbbe6f85cbed8c6fded69c713.png" width="32" height="32"> Ghost Recon Breakpoint
- ✏️ Last modification: 4/9/2026
- 💿 Platform: Steam
- 🛠️ Method: Proton

# Overview
Ghost Recon Breakpoint doesn't have a native port, works fine on Linux through Proton but it's partially locked behind Ubisoft Connect mandatory requeriment.
Ubisoft Connect is also not available on Linux natively, but it's possible to make it work through WINE.

If Ubisoft Connect it's working, GRB will work fine both on singleplayer and multiplayer.

The game shows greater stability on framerate with Vulkan on a AMD GPU compared to Windows 11.

# Guide
1. Download Window's Ubisoft Connect installer from official site: [https://www.ubisoft.com/es-mx/ubisoft-connect/download](https://www.ubisoft.com/es-mx/ubisoft-connect/download)
2. Install `protontricks` (If Arch user, open your terminal and run `yay -S protontricks`)
3. Run Protontricks and select "Ghost Recon Breakpoint: 2231380"
4. Choose "Install an application" and select UbisoftConnectInstaller.exe you downloaded.
5. Go through the installer and leave the default installation path (DO NOT CHANGE IT, otherwise it won't work and Protontricks is aware of it, it will show an error if you made a mistake)
6. Once done, you can close Protontricks.
7. In Steam, open properties menu on your Ghost Recon Breakpoint, automatic Proton version choosen by Steam should work fine, go to General and paste this on Launch parameters

```PROTON_ENABLE_WAYLAND=1 WINE_FULLSCREEN_FSR=1 VK_FORCE_IMAGE_FORMATS=1 %command%```

| Command | Function explained |
| ------------ | ------------ 
| %command% | Gamescope syntax | 
| PROTON_ENABLE_WAYLAND=1 | Evades issues with Wayland compositors | 
| WINE_FULLSCREEN_FSR=1 | Enables FSR and forces fullscreen mode | 
| VK_FORCE_IMAGE_FORMATS=1 | Forces the game to keep the rendering parameters who gets lost when booting Ubisoft Connect before the game itself | 

8. Go to your SteamLibrary folder (the one where you installed the game) and search this path: `/steamapps/compatdata/2231380/pfx/dosdevices/c:/users/steamuser/Documents/My Games/Ghost Recon Breakpoint/`, open GRB.ini with a text editor.
9. Change the following config:

WindowMode=1
DisplayWidth=1920
DisplayHeight=1080

Put WindowMode in 1 for borderless mode
DisplayWidth and DisplayHeight for the resolution you wanna play on, the game doesn't lets you change it in-game, so it should always be change here.

10. Save the file and run the game.
    
# Screenshots
<img src="https://github.com/Rammaken/rammaken-linux-gaming-guide/blob/main/screenshots/20260904215724_1.jpg">
