## Available in Proton 3.16 Beta:
###### 3.16-1:
- Rebased Proton patches onto Wine 3.16.
- Updated Vulkan support in Wine to 1.1.86, plus support for transform feedback.
- DXVK has been updated to [0.81](https://github.com/doitsujin/dxvk/releases/tag/v0.81) plus support for transform feedback which should fix missing models in many D3D11 games. *Transform feedback requires using Mesa git or NVIDIA's 396.54.09 Vulkan Beta driver*. 
- DXVK's d3d10 mode is now enabled by default.
- DXVK is now built as a native Linux library, which may give a small performance boost, and should make debugging easier for DXVK and driver developers.
- Missing textures for models in some VR games has been resolved.
- Ask the window manager to bypass the compositor in fullscreen mode. This may improve performance in some situations.
- All new makefile-based build system.
## Available in Proton 3.7:
###### 3.7-8:
- Minor compatibility fixes in preparation for future Proton versions.
###### 3.7-7:
- Improvements to alt-tab and fullscreen behavior in many games.
- Fix mouse behavior in some games and mice with high sample rates.
- Update DXVK to v0.80.
###### 3.7-6:
- Fix failure to start VR games.
- Improvements to fullscreen games running at non-native resolutions.
- Compatibility fix for games that use Steam integration.
- Return to previous D3D10 behavior in DXVK to allow games to fallback to D3D9.
###### 3.7-5:
- Performance improvements for timing APIs in CPU-limited scenarios
- Automatically capture mouse in fullscreen windows is enabled by default.
- More display ratios have smaller resolutions available.
- Fix a crash on old versions of SDL.
- Fix for mouse cursor drifting in Deus Ex.
- Debug script dump directory can be configured with `PROTON_DEBUG_DIR`.
- Further improvements to fullscreen focus and python3 compatibility.
###### 3.7-4:
- Support python3 as well as python2. This removes the requirement for python2 to be installed.
- DXVK updated to v0.70, view that changelog here: https://github.com/doitsujin/dxvk/releases DXVK's DX10 support is not yet enabled.
- Fullscreen games should more consistently gain keyboard focus on Ubuntu with gnome-shell. This can also help with games that auto-minimize on launch.
- Some useful default logging can be enabled with `PROTON_LOG=1 %command%` in the Steam game launch options. Logs will be dumped to $HOME/steam-$APPID.log. WINEDEBUG can still be set in user_settings.py for more extensive debugging.
- Debug scripts are no longer dumped to /tmp/ by default. They must now be enabled with `PROTON_DUMP_DEBUG_COMMANDS=1 %command%` in the Steam game launch options. They have also been moved to /tmp/proton_$USER/.
- Controllers will hopefully no longer cause long delays on startup on some systems (winehq bug 45084).
###### 3.7-3:
 - Fixed missing 32-bit libraries
###### 3.7-2:
 - Fixed debug DXVK
###### 3.7-1:
 - Initial release
