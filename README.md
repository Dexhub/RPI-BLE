#####
Raspberry Pi + BLE connection with iOS app
####


This is a PoC project repo. The script should perform the following:


- The script should start a UI screen and make the raspberry pi available to receive data.
- The UI should show:
    + The name/UUID of the raspberry Pi (top-label). 
- On receiving any data from the iOS app, the script should show an alert with the entire data received. This data should be json strings and can be higher than 250 bytes in length.
- The UI should have an option to write values to a GATT characteristic. The value to be written can be json string 400 bytes in length.
- A Readme for clean install.


Please use the following for this project:
- Python3
- guizero
- Inbuilt BLE chip for RPI 3+
- Pip3

