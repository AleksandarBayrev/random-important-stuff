# If you want to use `gamescope` and `gamescope` or `gamescopereaper` processes do not quit after you leave the game:
* Use the `gamescope-runner` script that is in `general-linux-fixes` repository
* Add `WINEDLLOVERRIDES="winedevice.exe=d"` to the launch options in Steam/environment variables in Heroic/Lutris

# If you want to pass adaptive sync do it like this:
* `--adaptive-sync -r 180`
* Example command: `gamescope-runner -w 3840 -h 2160 -W 2560 -H 1440 -f --adaptive-sync -r 180 -- mesa-custom-launcher 26.0.0-rc2 mangohud %command%`