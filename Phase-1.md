# Phase 1

### Objectives:

1. Get your feet wet
    - Create a README for the project that should have the below information:
    - Clear instructions on how to install a project on a fresh Raspbian OS
    - Updated requirements.txt
2. Replace QR codes to BLE
    - Use BLE to receive QR code based information from a nearby selected iOS device
        - This will allow the user to initiate actions from a nearby iOS app
        - Based on the actions, the data will be transmitted from an iOS app to the Raspberry Pi
        - The Raspberry Pi will take necessary actions and return the data to the iOS app using BLE.
    - Use BLE to send QR code information to a nearby selected iOS device:
        - This will allow the Raspberry Pi to send information back to the user on the iOS device.
        - Ensure that the data is read by the correct iOS device.
3. Code Cleanup
    - Cleanup existing code and write unit tests.
