# <img src="https://cdn2.steamgriddb.com/icon_thumb/eafd47a145d67a244ac72fa0617c3224.png" width="32" height="32"> Deadlock
- ✏️ Last modification: 4/9/2026
- 💿 Platform: Steam
- 🛠️ Method: Proton

# Overview
Deadlock despite being a Valve game doesn't have a native port yet (makes sense, still a closed beta) but works fine on Linux through Proton.

The game shows greater stability on framerate with Vulkan on a AMD GPU compared to Windows 11.

# Guide
1. In Steam, open properties menu on your Deadlock, go to Compatibility and force it, select Proton 11.0-2 (usually by default it may tray to run Steam Linux Runtime which will not work. Something related to a missing binary.)
2. In properties menu, go to General and paste this on Launch parameters

```gamescope -f -W 1920 -H 1080 -- %command% PROTON_ENABLE_WAYLAND=1 PROTON_LOCAL_SHADER_CACHE=1 -vulkan```

| Command | Function explained |
| ------------ | ------------ 
| gamescope -- %command% | Gamescope syntax, the parameters close around -- %command% | 
| -f | (Gamescope command) Forces the game to launch in fullscreen, without it, probably will open in windowed mode | 
| -W 1920 | (Gamescope command) Forces the internal display max resolution in width, switch 1920 for your monitor's max width | 
| -H 1080 | (Gamescope command) Forces the internal display max resolution in height, switch 1080 for your monitor's max height | 
| -f | (Gamescope command) Forces the game to launch in fullscreen, without it, probably will open in windowed mode | 
| PROTON_ENABLE_WAYLAND=1 | Evades issues with Wayland compositors | 
| PROTON_LOCAL_SHADER_CACHE=1 | Stores compiled shaders exclusively in the prefix (optional if you wish) | 
| -vulkan | (Source 2 engine parameter) Forces the game to launch in Vulkan renderer, it's easir for Proton running vulkan natively | 

If the game opens in fullscreen but with a lower resolution than your native, don't worry, if -W and -H commands are present, you should be able to change the resolution in-game without any issues.

# Screenshots
<img src="https://raw.githubusercontent.com/Rammaken/rammaken-linux-gaming-guide/refs/heads/main/screenshots/20260904215724_1.jpg">
