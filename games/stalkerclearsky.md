# <img src="https://cdn2.steamgriddb.com/icon/22b1cd168ec628442b3d4dc00fca434b/32/256x256.png" width="32" height="32"> S.T.A.L.K.E.R.: Clear Sky
- ✏️ Last modification: 5/9/2026
- 💿 Platform: Pirated / GOG DRM Free (as a Non-Steam game, may work  for Steam version too)
- 🛠️ Method: Proton

# Overview
S.T.A.L.K.E.R.: Clear Sky officially doesn't have a native port but there are some X-Ray Engine forks with full fledged Linux ports, in this guide I'll explain how to run the Windows version through Proton.

# Guide
1. Add xrEngine.exe as a non-Steam game on Steam, open properties of the game and set the following launch parameters: 
`PROTON_ENABLE_WAYLAND=1 -fsltx ../fsgame.ltx`

| Command | Function explained |
| ------------ | ------------ 
| PROTON_ENABLE_WAYLAND=1 | Evades issues with Wayland compositors | 
| -fsltx ../fsgame.ltx | Fixes the "Cannot open "fsgame.ltx" crash when launching. | 

2. In properties menu, go to Compatibility and force Proton 11.0-2.

3. Install `protontricks` (If Arch user, open your terminal and run `yay -S protontricks`)
4. Open Protontricks and choose your STALKER's Non-Steam shortcut.
5. Choose "Select the default wineprefix"
6. Choose "Install a Windows DLL or component" and install the following DLLs:
    - d3dcompiler_43
    - d3dcompiler_47
    - d3dx10
    - d3dx10_43
    - d3dx11_43
    - d3dx9
    - d3dx9_43
    - openal (Optional, for mods)
    - vcrun2022 (Optional, for mods)
    - directplay (Optional, for multiplayer)
      
This DLLs will fix the "Your system doesn't meets the minimum requeriments: Pixel Shader v1.1" crash when launching.

7. Run the game and should work into getting to the main menu without crashes, however, some people may experience a few issues here.

### **Issue 1:** Keyboard is not working
If your keyboard isn't working, can't move in-game or press ESC to skip intro cutscenes, it's not a Proton or issue with your desktop, it's a error within the game engine during the initial creation of the user configuration file where all the controls are unbinded by default.
To fix this, just head to Settings, go to Controls and hit the Default button, this will bind all keys to their default ones, then Apply and should be fixed.

### **Issue 1:** Resolution is not configured correctly and it's preventing from moving my mouse.
This issue can be fixed in two ways, through the games settings itself by switching it to your native resolution, however many people may experience a problem where if the mouse moves vertically will get reset to the center, preventing you from doing anything at all.

In this case, head to the Proton's prefix folder that was generated for your game, should be a path like this:
`/home/rammaken/.steam/steam/steamapps/compatdata/3165295408/pfx/dosdevices/c:/users/rammaken/docu~owl/stal~wtn/`
(Rammaken is my user and 3165295408 the ID steam assigned to this game, this will vary on your system so search for it manually using this one as reference.)

Open `user.ltx` with a text editor, search and change the following line:

`vid_mode 1920x1080`

Change 1920x1080 for your resolution, save the file and run your game to check if it works

# Screenshots
<img src="https://raw.githubusercontent.com/Rammaken/rammaken-linux-gaming-guide/refs/heads/main/screenshots/20260905200603_1.jpg">
<img src="https://raw.githubusercontent.com/Rammaken/rammaken-linux-gaming-guide/refs/heads/main/screenshots/20260905200825_1.jpg">
