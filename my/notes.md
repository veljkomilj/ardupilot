# Notes

## Linux Mint doesn't have python in it's environment
Modify "#!/usr/bin/env python" to "#!/usr/bin/env python3" in all ardupilot repository files.

## Running sim_vehicle.py doesn't show UI

First investigate why mavproxy.py is failing by enbaling debug information:
```
../Tools/autotest/sim_vehicle.py --map --console -m "--moddebug=3"
```

Log will show up that python can't find wx module. This has to be installed with apt:
```
sudo apt install python3-wxgtk4.0
```
