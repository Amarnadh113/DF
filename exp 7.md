Ex.No.7 – Use AFLogical OSE to Extract Data from an Android Device

Aim

To extract logical data such as contacts, SMS, MMS and call logs from an Android device using AFLogical OSE.

Requirements

- Android device
- USB cable
- Computer
- Java
- Android Debug Bridge (ADB)
- AFLogical OSE
- USB debugging enabled

Step 1 – Prepare the Environment

Install Java and Android Debug Bridge (ADB) on the computer.

Enable USB Debugging on the Android device:

1. Open Settings.
2. Go to About Phone.
3. Tap Build Number seven times.
4. Open Developer Options.
5. Enable USB Debugging.

Step 2 – Connect the Android Device

Connect the Android device to the computer using a USB cable.

Open Command Prompt or Terminal and execute:

adb devices

The connected device should be displayed.

Example:

List of devices attached
ABC123456789    device

If the device is shown as "device", the connection is successful.

Step 3 – Verify ADB Connection

Check the Android device information:

adb shell getprop ro.product.model

Check the Android version:

adb shell getprop ro.build.version.release

These commands confirm that the computer can communicate with the Android device.

<img width="1600" height="726" alt="WhatsApp Image 2026-09-21 at 11 58 57 PM" src="https://github.com/user-attachments/assets/faaa2e0c-10ea-4ac3-81a6-b552a1f7c48f" />


Step 4 – Prepare AFLogical OSE

Download and extract AFLogical OSE on the computer.

Navigate to the AFLogical OSE directory:

cd AFLogical

Check the available files:

dir

For Linux/macOS:

ls

Step 5 – Run AFLogical OSE

Launch the AFLogical OSE application according to the version/package provided for the experiment.

The tool communicates with the connected Android device through ADB and performs logical extraction.

The extraction may include:

- Contacts
- Call logs
- SMS
- MMS
- Other supported application data

Step 6 – Select Data for Extraction

Select the required data categories in AFLogical OSE.

Example:

Contacts       ✓
Call Logs      ✓
SMS            ✓
MMS            ✓

Start the extraction process.

Step 7 – Save the Extracted Data

Choose a destination folder on the computer.

Example:

C:\Android_Forensics\AFLogical_Output\

The extracted files are saved in the selected output directory.

Example structure:

AFLogical_Output/
│
├── Contacts
├── Call_Logs
├── SMS
└── MMS

Step 8 – Examine the Extracted Data

Open the generated output files and examine the extracted information.

The investigator can identify:

- Contact names and numbers
- Incoming and outgoing calls
- SMS messages
- MMS information
- Timestamps
- Other available logical evidence

<img width="1600" height="720" alt="WhatsApp Image 2026-09-21 at 11 58 58 PM" src="https://github.com/user-attachments/assets/57de0ccd-02b0-4439-abd4-a16166906214" />

Step 9 – Preserve the Evidence

Store the extracted data in a secure location.

Do not modify the original extracted evidence.

Maintain proper documentation of:

- Device information
- Extraction date and time
- Tool used
- Output location
- Evidence identifier

Important ADB Commands

adb devices

Displays connected Android devices.

adb shell getprop ro.product.model

Displays the device model.

adb shell getprop ro.build.version.release

Displays the Android version.

adb shell

Opens a shell on the connected Android device.

Expected Output

The extraction produces logical evidence such as:

Contacts
Call Logs
SMS
MMS
Device Information

Result

The Android device was successfully connected to the computer using ADB, and logical data such as contacts, SMS, MMS and call logs was extracted using AFLogical OSE.

Conclusion

AFLogical OSE can be used as a logical acquisition tool for supported Android devices. It helps investigators collect available user data while documenting the extraction process for forensic analysis.
