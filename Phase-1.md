######
Phase 1
######

Objectives:
A - Create a README for the project that should have the below information:
    - Clear instructions on how to install a project on a fresh Raspbian OS
    - Updated requirements.txt
B - Add BLE Workflow in the existing code:
    - Use BLE to receive QR code based information from a nearby selected iOS device
        - This will allow the user to initiate actions from a nearby iOS app
        - Based on the actions, the data will be transmitted from an iOS app to the Raspberry Pi
        - The Raspberry Pi will take necessary actions and return the data to the iOS app using BLE.
    - Use BLE to send QR code information to a nearby selected iOS device:
        - This will allow the Raspberry Pi to send information back to the user on the iOS device.
        - Ensure that the data is read by the correct iOS device.
C - Code Cleanup:
    - Cleanup existing code and write unit tests.

