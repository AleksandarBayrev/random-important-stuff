# Use `taskset` to limit number of cores a process is using, example:
* `taskset -c 0,1,2,3` to use 4 cores (or 2 cores 2 threads)
# If using a Windows application in that case the example will be:
* `taskset -c 0,1,2,3 %command%`
# If `taskset` is crashing the application use `WINE_CPU_TOPOLOGY` environment variable (check if it is used still)
* `WINE_CPU_TOPOLOGY=4:0,1,2,3 %command%`
# PES 2019
* To install it via Lutris run winetricks and install `vcrun6sp6` and `mfc42`