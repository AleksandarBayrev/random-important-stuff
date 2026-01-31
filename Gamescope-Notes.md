# If you want to use `gamescope` and `gamescope` or `gamescopereaper` processes do not quit after you leave the game:
* Use the `gamescope-runner` script that is in `general-linux-fixes` repository (and still check for phantom `gamescope` and `gamescopereaper` processes, since sometimes if the game crashes for example, or you force quit - these are not killed)
* Always pass the `-r` option (refresh rate), match it to your monitor's refresh rate
* Example command: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch -r 180 --expose-wayland --`
* Pass `--adaptive-sync` if the display supports VRR
* Example command: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch -r 180 --adaptive-sync --expose-wayland --`
* If you want to stretch the screen use the `-S stretch` switch: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch -r 180 --adaptive-sync --expose-wayland --`
* Add `WINEDLLOVERRIDES="winedevice.exe=d"` to the launch options in Steam/environment variables in Heroic/Lutris

# For Heroic Games Launcher you should do it like this:
![alt text](heroic-gamescope.png)
* `/home/aleksandar/.local/bin/gamescope-runner` is the wrapper command (full path to `gamescope-runner`) and the arguments should be passed like this: `-w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch -r 180 --adaptive-sync --expose-wayland --` (note the `--` at the end)

# If you want to use `mangohud` install `mangoapp` as well and make a symbolic link to the already configured `mangohud`: `$HOME/.config/MangoHud/MangoHud.conf` to `$HOME/.config/MangoHud/mangoapp.conf` => `ln -s $HOME/.config/MangoHud/MangoHud.conf $HOME/.config/MangoHud/mangoapp.conf`
* Example command: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch -r 180 --adaptive-sync --expose-wayland --mangoapp -- mesa-custom-launcher 26.0.0-rc2 %command%`
* If `--mangoapp` switch doesn't work run it from `mangohud`, example command: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch -r 180 --adaptive-sync --expose-wayland -- mesa-custom-launcher 26.0.0-rc2 mangohud %command%`

# If you want to pass adaptive sync do it like this:
* `--adaptive-sync -r YOUR_REFRESH_RATE`
* Example command: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch -r 180 --adaptive-sync --expose-wayland -- mesa-custom-launcher 26.0.0-rc2 %command%`

# If some games have problems with the mouse append `--force-grab-cursor`

# For `Steam` do not forget to add `%command%`, example: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f -S stretch -r 180 --adaptive-sync --expose-wayland -- %command%`