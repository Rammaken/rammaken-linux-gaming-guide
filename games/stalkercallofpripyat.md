# <img src="https://cdn2.steamgriddb.com/icon/321cf86b4c9f5ddd04881a44067c2a5a/32/256x256.png" width="32" height="32"> S.T.A.L.K.E.R.: Call of Pripyat
- ✏️ Last modification: 17/11/2026
- 💿 Platform: Pirated
- 🛠️ Method: Non-Steam

# Overview
S.T.A.L.K.E.R.: Call of Pripyat runs out of the box with Proton on Steam. However modified engines like IX-Ray doesn't work.

# Guide
1. Add xrEngine.exe as a non-Steam game on Steam, open properties of the game and set the following launch parameters: 
`-fsltx ../fsgame.ltx`

| Command | Function explained |
| ------------ | ------------ 
| -fsltx ../fsgame.ltx | Fixes the "Cannot open "fsgame.ltx" crash when launching. | 

2. In properties menu, go to Compatibility and force Proton 11.0-2.

If experincing "Your system doesn't meets the minimum requeriments: Pixel Shader v1.1" crash when launching, do the following:

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
      

