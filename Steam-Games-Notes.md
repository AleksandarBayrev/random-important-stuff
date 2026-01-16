# Black Mesa
* Add `fps_max 100` to `$SteamLibrary/steamapps/common/Black Mesa/bms/cfg/server.cfg` to limit FPS globally.
# Serious Sam 2
* Under Linux use `+gfx_iAPI 1` in the start options: `%command% +gfx_iAPI 1`
# Among Us
* Under Linux use the launch option: `PROTON_USE_WINED3D=1 %command%`
# Fable - The Lost Chapters
* Under Linux use the launch option: `PROTON_USE_WINED3D=1 %command%`
# CS GO (legacy)
* Under Linux use the launch option: `SDL_VIDEO_DRIVER=wayland RADV_PERFTEST=gpl %command% -steam -vulkan -high -novid -nojoy` and uncap the FPS of the game (`fps_max 0`)