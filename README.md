#####
Raspberry Pi + BLE connection with iOS app
####


This is a PoC project repo. The script should perform the following:


- The script should start a UI screen and make the raspberry pi available to receive data.
- The UI should show:
    + The name/UUID of the raspberry Pi (top-label). 
    + The list of devices nearby to communicate to.
- On receiving any data from the iOS app, the script should show an alert with the entire data received
- On selecting one of the devices from the nearby list, it should be able to send the data to that device.
- The data for now can be a static string.
- A Readme for clean install.


Please use the following for this project:
- Python3
- guizero
- Inbuilt BLE chip for RPI 3+
- Pip3 for requirements

