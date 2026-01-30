# Use `taskset` to limit number of cores a process is using, example:
* `taskset -c 0,1,2,3` to use 4 cores (or 2 cores 2 threads)
# If using a Windows application in that case the example will be:
* `taskset -c 0,1,2,3 WINE_CPU_TOPOLOGY=4:0,1,2,3 %command%`