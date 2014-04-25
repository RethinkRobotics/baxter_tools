1.0.0 (2014-5-1)
---------------------------------
- Updates baxter_tools scripts to verify software version compatibility
- Updates update_robot adding instructions for attaching grippers before proceeding with update
- Fixes update_robot timeout for identifying available updates by increasing timeout to five seconds

0.7.0 (2013-11-21)
---------------------------------
- Creation of baxter_tools repository from sdk-examples/tools.
- Package restructure in support of Catkin expected standards.
- Adds camera_control from previous location in baxter_examples.
- Adds check for grippers pre-tare/calibrate.
- Adds reset to camera_control tool. Useful when not all cameras enumerated at boot.
- Fixes tucks arms allowing for clean handling of interrupts and partial tucks.

