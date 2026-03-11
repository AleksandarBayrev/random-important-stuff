# CS:GO Launch Options
## For Linux this is what I found out works the best with OpenGL
* `SDL_VIDEO_DRIVER=wayland RADV_PERFTEST=gpl %command% -steam -vulkan -high -novid -nojoy +exec csgo`
* Copy `csgo.cfg` to `$GAMEDIR/csgo/cfg`
## If the game crashes on startup use this as a prefix to the command above, so basically use this:
* `LD_PRELOAD="/mnt/OtherStuff/SteamLibrary/steamapps/common/Counter-Strike Global Offensive/bin/linux64/libtcmalloc_minimal.so.4" gamemoderun %command% -novid -nojoy` where the path of `libtcmalloc_minimal.so.*` is from CS:GO's path, check it in the file manager.
## Add `-nopreload -nopreloadmodels -nopreloadsounds` to launch parameters for RX 6000 series GPUs