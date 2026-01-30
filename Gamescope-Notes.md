# If you want to use `gamescope` and `gamescope` or `gamescopereaper` processes do not quit after you leave the game:
* Use the `gamescope-runner` script that is in `general-linux-fixes` repository (and still check for phantom `gamescope` and `gamescopereaper` processes, since sometimes if the game crashes for example, or you force quit - these are not killed)
* Example command: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f --expose-wayland --`
* If you want to stretch the screen use the `-S stretch` switch: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch --expose-wayland --`
* Add `WINEDLLOVERRIDES="winedevice.exe=d"` to the launch options in Steam/environment variables in Heroic/Lutris

# For Heroic Games Launcher you should do it like this:
![alt text](heroic-gamescope.png)
* `/home/aleksandar/.local/bin/gamescope-runner` is the wrapper command (full path to `gamescope-runner`) and the arguments should be passed like this: `-w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch --expose-wayland --` (note the `--` at the end)

# If you want to pass adaptive sync do it like this:
* `--adaptive-sync -r YOUR_REFRESH_RATE`
* Example command: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f --adaptive-sync -r 180 -S stretch --expose-wayland -- mesa-custom-launcher 26.0.0-rc2 mangohud %command%`

# If some games have problems with the mouse append `--force-grab-cursor`

# For `Steam` do not forget to add `%command%`, example: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f --expose-wayland -- %command%`