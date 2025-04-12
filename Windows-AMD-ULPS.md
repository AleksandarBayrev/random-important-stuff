# In order not to crash the GPU when entering into ultra-low power state when the monitors are off:
* Open `regedit`
* Find `EnableULPS`
* Set it to `0`
* Click on `Find Next` and check every occurence if is it 0 for GPU/Video.