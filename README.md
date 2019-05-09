#####
Raspberry Pi + BLE connection with iOS app
####


# Phase 1

Background:
    - The project is about creating a python based BLE peripheral program that runs on Raspberry Pi. The program acts as a BLE peripheral device and waits for a connection from an iOS app. Once its connected it reads JSON  based string data passed by the iOS app processes it and sends information back. The program has other functionalities for encryption and signing which is the processing part. The program is already developed and so is the iOS app. The program has a UI and uses QR code to communicate with the iOS app. The idea is to instead use BLE to communicate to the mobile app.

### Objectives:

1. Instructions on how to install the program on a fresh raspbian image:
    - I created this project sometime ago and had to do a few hacks on raspbian 
      to enable opencv2 on the raspberry pi. I might still have the instructions
      somewhere, but you'd need to install it first to proceed to second objective.
    - Update requirements.txt

2. Support the following BLE flows:
    - Securely Link to an iOS app
    - Securely UnLink from an iOS app
    - Sync data between the Raspberry Pi and iOS app.
    - Process the data sent from an iOS app, when a transfer flow is initiated on the iOS device.
    - Send the results back from the Raspberry Pi to the iOS device.

3. Code Cleanup
    - Cleanup existing code and write unit tests.

Please use the following for this project:
- Python3
- guizero
- Inbuilt BLE chip for RPI 3+
- Pip3

## More information on each BLE work flow:

    A. Securely Link to an iOS app.
    - In this workflow, an iOS app will start searching for a RPI device for linking.
    - Based on a matching UUID, it will send a request to the RPI device.
    - The python program will generate 6 random digits and will be shown on the screen. 
    The iOS app needs to manually confirm the numbers and write them to RPI device for verification. This will ensure that the iOS user is authenticated.
    - After this the RPI should indicate that the hardware is successfully paired to the iOS app.
    - 1 RPI device can only pair to a single iOS app.
    - 1 iOS app can pair to multiple RPI devices.
    - The user will also be able to name/rename the RPI hardware which will be shown on the python UI.

    B. Securely Unlink from an iOS app.
    - In this workflow, an iOS app will first connect to an already paired RPI device.
    - It will then send a request to unlink to the RPI.
    - The request would need to be validated using a passcode on the RPI screen.
    - If the passcode matches, the raspberry pi would delete the link between the iOS app and will send a notification to the iOS app to do the same.

    C. Sync data between the RaspberryPi and iOS app.
    - In this workflow, an iOS app will first send a sync request to the raspberry pi.
    - The raspberry pi will ask the user to enter the correct passcode and based on that allow the sync request to proceed.
    - All the "accounts" related meta data will be transferred to the iOS app.
    - Once the data sync is finished, both the devices will let each other know.

    D. Process the data sent from an iOS app, when a transfer flow is initiated on the iOS device.
    - The iOS device will initate a new workflow and send the related information to the raspberry pi for processing.
    - Based on this, the user will be asked to enter the passcode to unlock the device and authorize the data processing.
    - Once the data is processed, the results will be sent back to the iOS app.


## FAQs:
1 - How will you pick a candidate ?
- Depends on the candidates:
        - Past experience with similar projects, portfolio.
        - Communication
        - Responsiveness
        - Knowledge in this area
2 - What happens after you pick a freelancer?
    - You will need to send me your full name, Company name, people who will be involved with the project.
    - I'll share the NDA and the Statement of Work.
    - You would need to sign both of them and along with them send me the following things:
        - Github handle of the person who will be developing the project
        - Email addresses of the person who will be involved in the project.
    - After signing both documents, I'll provide you with the following:
        - Access to github repo.
        - Add you the project's Jira board for tracking.
        - Add you to the project's slack channel.
3 - What is the development process? (Agile/Sprint based) 3 - 7 day sprints
    - Each feature listed in the SOW will be broken into separate tasks.
    - You will need to estimate the effort for each of the tasks assigned to you before beginning work on it.
    - Time will be tracked using workdiary or hubstaff; as it would have been discussed prior to the contract.
    - We will be having a 15 minute sync up everyday on the tasks of the day. We will decide on the time before the start of the work.
    - For each major epic, you will create a separate feature branch on git and commit your changes there. Once the changes are done, and test cases are added, you can demo them in the next day's sync up. Once the demo is done, and no more changes are suggested, you may pull all the changes from master into your current branch and test it. Once it looks good, after an internal code review please raise a pull request with all the detail on your changes.
    - I will then review your code and merge it to master. This will be done for each epic and major tasks.
    - Never commit on Master or force push your changes on master.
4 - How will the payments be handled.
    - You will need to push all your current changes to the remote repo by wednesday and saturday of every week; to keep things current.
    - If I do not see repo updated on regular basis the contract will be paused and potentially revoked.

5 - License requirements:
- This is a work made of hire hence your work is the property of us once its done. Consultant shall make no claims of the ownership of the work and assign irrevocable rights to that work to us.
- Consultant will make sure that your work is original and not a copy of someone else's original work.
- Consultant will make sure that all the necessary licenses are checked before submitting someone else's work.
- Consultant warrants that (a) the Services will be performed in a professional and workmanlike manner consistent with industry standards; (b) all work under this Agreement will be Consultant’s original work, and neither the Services nor any Company Inventions, nor any development, use, production, distribution or exploitation thereof, will infringe, misappropriate or violate any intellectual property or other rights of any person or entity (including, without limitation, Consultant); (c) Consultant has the full right to provide the Company with the assignments and rights provided for herein and otherwise to fully perform Consultant’s obligations under this Agreement; (d) Consultant will have each person who may be involved in any way with, or have any access to, any Services or Confidential Information enter into (prior to any such involvement or access) a binding agreement for the Company's benefit that is at least as protective of the Company’s rights as provided herein; (e) Consultant will comply with all applicable laws and regulations in the course of performing the Services; and (f) Consultant has obtained, and will maintain in full force and effect, any licenses that may be required to perform the Services.
