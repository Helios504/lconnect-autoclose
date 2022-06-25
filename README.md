# lconnect-autoclose
Lian Li LConnect Auto Close After Start

# Overview
The Lian Li L-Connect software uses CPU whilst running idle in windows which is not ideal. L-Connect is used to configure Lian Li Unifans via the Unihub.
L-Connect is only required on startup to configure the Unihub RGB settings, it can be closed after it has started and completed its configuration.

This repository contains a preconfigured Windows Task Schedular configuration that executes a bat file on startup which launched L-Connect.
After 15 seconds L-Connect is then closed automatically.

# Installation
The following instructions are for L-Connect 3, however for L-Connect 2 simply use the files with L-Connect 2 in the name instead.

1. Download 'Start Stop L-Connect 3.xml' and 'startstop_lconnect3.bat' from this repository
2. Move the startstop_lconnect3.bat file into a memorable location. In this example it is "D:\Apps\"
3. Open Task Scheduler (you can search via the Windows start menu)
4. Right click on task schuedular library in the left hand panel
5. Select "Import Task"
6. Locate "Start Stop L-Connect 3.xml"
7. If you didnt use "D:\Apps" as your storage location for the script. Right click on the task scheduler entry named Start Stop L-Connect 3 and press properties
8. Navigate to the "Actions" tab
9. Click "edit" on the first entry
10. Replace "D:\Apps" with your location in the "Program/Script" and "Start in" fields.
11. Click ok and close the Window

# Testing
- To test if your configuration is setup correctly, right click on the task schedular entry and press "Run".
You should see a command prompt window launch, L-Connect 3 should start up (hidden in the system tray). Then it should close 15 seconds later.
- Alternatively you can reboot your PC and upon login L-Connect should start and then close.



