# <img src="https://cdn2.steamgriddb.com/icon/713fd63d76c8a57b16fc433fb4ae718a/32/1024x1024.png" width="32" height="32"> Ghost of Tsushima
- ✏️ Last modification: 7/9/2026
- 💿 Platform: Pirated
- 🛠️ Method: Non-Steam game

# Overview
Ghost of Tsushima doesn't have a native linux port so it needs to be run through Proton, for this guide I downloaded the game from DODI repacks and installed it through Heroic Games Launcher.

# Guide
1. Open Steam and add Ghost of Tsushima as a Non-Steam game.
2. Open the Properties menu and go to Compatibility, force Proton 11.0-2 (This fixes the Pixel Shader v6.6 support crash when launching).
3. Go to Shortcut and paste the following launch parameters: `gamescope -f -W 1920 -H 1080 -- %command% PROTON_ENABLE_WAYLAND=1 -nolauncher -useallavailablecores`

| Command | Function explained |
| ------------ | ------------ 
| gamescope -f | (Gamescope command) Forces fullscreen, some people won't need this tho. | 
| -W 1920 |  (Gamescope command) Forces internal render width resolution to 1920. Change to your native res. | 
| -H 1080 |  (Gamescope command) Forces internal render height resolution to 1080. Change to your native res. | 
| PROTON_ENABLE_WAYLAND=1 | Evades issues with Wayland compositors. | 
| -nolauncher | (GoT engine command) Skips the initial launcher, you won't really need that. | 
| -useallavailablecores | (GoT engine command) (Optional) Lets the game use all the CPUs cores, this can help a lot with performance if running a Intel Xeon | 

# Screenshots
<img src="https://raw.githubusercontent.com/Rammaken/rammaken-linux-gaming-guide/refs/heads/main/screenshots/20260906185441_1.jpg">
<img src="https://raw.githubusercontent.com/Rammaken/rammaken-linux-gaming-guide/refs/heads/main/screenshots/20260906192451_1.jpg">
