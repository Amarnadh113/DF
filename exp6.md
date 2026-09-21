Ex. No: 6 – Use Sleuth Kit to Analyze Digital Evidence

Aim

To analyze a disk image and recover digital evidence using The Sleuth Kit (TSK) command-line tools.



Software Required

- Sleuth Kit (TSK)
- Windows OS
- Command Prompt
- FTK Imager – for acquiring disk images
- OSFMount – optional
- Evidence files:
  - "4Dell Latitude CPi.E01"
  - "4Dell Latitude CPi.E02"

Procedure

Step 1: Install Sleuth Kit

Download and install Sleuth Kit for Windows.

After installation, open Command Prompt and navigate to the Sleuth Kit installation directory.

cd "C:\Program Files\Sleuth Kit\bin"

Check whether Sleuth Kit is working:

fsstat -V

---




<img width="1917" height="1037" alt="Screenshot 2026-09-21 223225" src="https://github.com/user-attachments/assets/f4fbd334-144e-4020-9efc-50183248a1e2" />


Step 2: Acquire the Disk Image

The disk image can be created using FTK Imager.

The evidence image used in this experiment is:

4Dell Latitude CPi.E01
4Dell Latitude CPi.E02

Keep both files in the same folder.

Example:

C:\Evidence\
    4Dell Latitude CPi.E01
    4Dell Latitude CPi.E02

---

<img width="1902" height="962" alt="Screenshot 2026-09-21 223247" src="https://github.com/user-attachments/assets/775b814d-4afd-4e23-b44e-d4c54575cff4" />


Step 3: Identify the File System

Use the "fsstat" command to obtain file-system information.

fsstat "C:\Evidence\4Dell Latitude CPi.E01" > filesystem_info.txt

This displays information such as:

- File-system type
- Block size
- Inode information
- File-system structure

---


<img width="1907" height="1030" alt="Screenshot 2026-09-21 223312" src="https://github.com/user-attachments/assets/202ed425-e84b-4836-86a1-4a7056e1b865" />


Step 4: List Partitions

Use "mmls" to identify partitions in the disk image.

mmls "C:\Evidence\4Dell Latitude CPi.E01" > partitions.txt

The output contains:

- Partition start sector
- Partition end sector
- Partition size
- Partition type

---

Step 5: List Files and Directories

Use "fls" to recursively list files and directories.

fls -r "C:\Evidence\4Dell Latitude CPi.E01" > file_list.txt

To include deleted files:

fls -r -d "C:\Evidence\4Dell Latitude CPi.E01" > deleted_files.txt

The output can be examined to identify suspicious or deleted files.

---

Step 6: Recover a File

First, identify the required file's inode number from the "fls" output.

Then use "icat" to recover the file:

icat "C:\Evidence\4Dell Latitude CPi.E01" INODE_NUMBER > recovered_file

Example:

icat "C:\Evidence\4Dell Latitude CPi.E01" 12345 > recovered.txt

Replace "12345" with the actual inode number.

---

Step 7: Analyze File Metadata

Use "istat" to examine metadata associated with an inode.

istat "C:\Evidence\4Dell Latitude CPi.E01" INODE_NUMBER > metadata_info.txt

Example:

istat "C:\Evidence\4Dell Latitude CPi.E01" 12345 > metadata_info.txt

The metadata may contain:

- File size
- File type
- File allocation status
- Modified time
- Access time
- Metadata-change time

---

Step 8: Create a Timeline

Generate a body file using "fls":

fls -m / -r "C:\Evidence\4Dell Latitude CPi.E01" > body.txt

Then create a timeline using "mactime":

mactime -b body.txt > timeline.txt

The timeline helps analyze:

- Modified time
- Accessed time
- Changed time
- File activity

---

Important Sleuth Kit Commands

Command| Purpose
"fsstat"| Displays file-system information
"mmls"| Displays partition information
"fls"| Lists files and directories
"icat"| Recovers/extracts file content
"istat"| Displays inode metadata
"mactime"| Creates a file activity timeline

Complete Command Set

fsstat "C:\Evidence\4Dell Latitude CPi.E01" > filesystem_info.txt

mmls "C:\Evidence\4Dell Latitude CPi.E01" > partitions.txt

fls -r "C:\Evidence\4Dell Latitude CPi.E01" > file_list.txt

fls -r -d "C:\Evidence\4Dell Latitude CPi.E01" > deleted_files.txt

istat "C:\Evidence\4Dell Latitude CPi.E01" INODE_NUMBER > metadata_info.txt

icat "C:\Evidence\4Dell Latitude CPi.E01" INODE_NUMBER > recovered_file

fls -m / -r "C:\Evidence\4Dell Latitude CPi.E01" > body.txt

mactime -b body.txt > timeline.txt

Expected Output

The analysis produces the following evidence files:

<img width="1461" height="761" alt="Screenshot 2026-09-21 223143" src="https://github.com/user-attachments/assets/17d3b5ee-9de2-452e-b48d-9cc9c4ff3ec2" />

filesystem_info.txt
partitions.txt
file_list.txt
deleted_files.txt
metadata_info.txt
body.txt
timeline.txt
recovered_file


Result

The disk image was successfully analyzed using The Sleuth Kit. File-system information, partitions, file listings, metadata, deleted files, recovered files, and file activity timelines were obtained from the digital evidence.

Conclusion

Sleuth Kit provides command-line forensic tools for examining disk images while preserving the original evidence. The extracted information can be used to identify and document relevant digital evidence during a forensic investigation.
