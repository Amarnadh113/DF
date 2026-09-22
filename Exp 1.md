# Digital Forensics – Evidence Acquisition Using FTK Imager

## Experiment No. 1

### Aim
To acquire volatile and non-volatile digital evidence using AccessData FTK Imager.

## Introduction
FTK Imager is a Windows-based digital forensics tool used to acquire and analyze computer forensic evidence. It can be used to acquire volatile memory (RAM) and non-volatile memory such as hard disk images.

## Types of Evidence Acquisition

1. **Volatile Memory Acquisition**
   - Captures the contents of RAM.
   - The acquired memory is saved with a `.mem` extension.
   - Pagefile and AD1 files can also be included.

2. **Non-Volatile Memory Acquisition**
   - Creates a forensic disk image of storage devices.
   - FTK Imager can acquire:
     - Physical drives
     - Logical drives
     - Image files
     - Contents of folders
     - CDs/DVDs

## Procedure

### A. Acquiring Volatile Memory

1. Open FTK Imager.
2. Select **Capture Memory**.
3. Select the destination folder.
4. Enter the destination filename.
5. Select **Include pagefile** if required.
6. Select **Create AD1 file** if required.
7. Click **Capture Memory**.
8. Wait until the memory acquisition is completed.
9. The captured memory is saved as a `.mem` file.

### B. Acquiring a Disk Image

1. Open FTK Imager.
2. Select **Create Disk Image**.
3. Select the required source type.
4. Select **Physical Drive** to acquire a complete physical drive.
5. Select the required drive.
6. Click **Finish**.
7. Select the required image format.
8. Enter the case details.
9. Select the destination folder.
10. Enter the image filename.
11. Set the image fragment size.
12. Enable **Verify images after they are created**.
13. Click **Start** to begin acquisition.
14. Wait for the acquisition to complete.
15. Verify the hash values.


<img width="342" height="241" alt="ftk 1" src="https://github.com/user-attachments/assets/3f9ff194-59a8-4bda-a605-9c62a6a8eb1a" />




<img width="679" height="550" alt="ftk 2" src="https://github.com/user-attachments/assets/a6406d39-1380-40d3-b79c-6629ef22454f" />




<img width="679" height="543" alt="ftk 3" src="https://github.com/user-attachments/assets/d7657a2e-6f64-4591-b3d0-ceabd33ff07c" />




<img width="685" height="492" alt="ftk 4" src="https://github.com/user-attachments/assets/37120c8f-ddfc-4ee5-876f-07eb60c266fd" />




<img width="694" height="493" alt="ftk 6" src="https://github.com/user-attachments/assets/c15ea1c8-f1e8-4308-bcd3-c2de0297ff10" />




<img width="702" height="598" alt="gftk 7" src="https://github.com/user-attachments/assets/3ee5c78f-e469-4924-aedb-12b711518dda" />




<img width="618" height="442" alt="ftk 8" src="https://github.com/user-attachments/assets/d69b8895-85e2-47ed-8b3a-b469f4a23a4e" />




<img width="651" height="387" alt="ftk 9" src="https://github.com/user-attachments/assets/6b1d7984-0d01-4bc7-b18a-754575882765" />




<img width="1600" height="453" alt="ftk 10" src="https://github.com/user-attachments/assets/b9d04975-3c90-40bd-ade5-28864efb4395" />




<img width="1461" height="1077" alt="5" src="https://github.com/user-attachments/assets/6264e6df-9654-4177-9c7a-11ab41b14eb8" />





## Image Formats

### Raw (dd)
A commonly used raw forensic image format. It does not contain headers or metadata.

### SMART
A disk image format designed for Linux file systems.

### E01
A proprietary forensic image format developed by Guidance Software's EnCase. It supports compression and contains case information and hash values.

### AFF
Advanced Forensic Format (AFF), designed to avoid dependence on a proprietary format.

## Importance of Hash Verification

Hash verification is used to check the integrity of the acquired evidence. After acquisition, the hash values are matched to ensure that the evidence has not been altered.

## Result

The volatile memory and disk image were successfully acquired using FTK Imager, and the hash values were verified to maintain the integrity of the digital evidence.

## Tool Used

- AccessData FTK Imager
- Windows Operating System

## Conclusion

FTK Imager provides a method for acquiring digital forensic evidence from volatile memory and storage devices while maintaining evidence integrity through hash verification.
