# lconnect-autoclose
Lian Li LConnect Auto Close After Start

# Overview
The Lian Li L-Connect software uses CPU whilst running idle in windows which is not ideal. L-Connect is used to configure Lian Li Unifans via the Unihub.
L-Connect is only required on startup to configure the Unihub RGB settings, it can be closed after it has started and completed its configuration.

This repository contains a preconfigured Windows Task Schedular configuration that executes a bat file on startup which launched L-Connect.
After 15 seconds L-Connect is then closed automatically.

# Installation
The following instructions are for L-Connect 3, however for L-Connect 2 simple use the files with L-Connect 2 in the name instead.

* Download 'Start Stop L-Connect 3.xml' and 'startstop_lconnect3.bat' from this repository
* Move the startstop_lconnect3.bat file into a memorable location. In this example it is "D:\Apps\"
* Open Task Scheduler (you can search via the Windows start menu)
* Right click on task schuedular library in the left hand panel
* Select "Import Task"
* Locate "Start Stop L-Connect 3.xml"
* If you didnt use "D:\Apps" as your storage location for the script. Right click on the task scheduler entry named Start Stop L-Connect 3 and press properties
* Navigate to the "Actions" tab
* Click "edit" on the first entry
* Replace "D:\Apps" with your location in the "Program/Script" and "Start in" fields.
* Click ok and close the Window

# Testing
To test if your configuration is setup correctly, right click on the task schedular entry and press "Run".
You should see a command prompt window launch, L-Connect 3 should start up (hidden in the system tray). Then it should close 15 seconds later.
Hopefully your RGB was configured during this time.
