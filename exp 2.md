# Experiment 2: Recover Deleted or Damaged Files from a Storage Device Using TestDisk

## Aim

To recover deleted or missing partitions and repair a corrupted partition or damaged NTFS boot sector from a storage device using **TestDisk**.

## Software Used

* TestDisk
* Linux Operating System

## Introduction

TestDisk is an open-source data recovery and disk repair utility used to recover lost partitions and make non-booting disks bootable again.

TestDisk can be used to:

* Recover deleted or lost partitions
* Recover damaged partition tables
* Repair corrupted file systems
* Recover deleted files
* Repair NTFS boot sectors
* Recover partitions from damaged storage devices
* Restore partition structures

In this experiment, TestDisk was used on a **Linux operating system** to analyze a storage device, search for missing partitions, verify the contents of the recovered partition, restore the correct partition status, and repair a damaged NTFS boot sector.

## Procedure

### Step 1: Open TestDisk

Open the **Terminal** in the Linux operating system and launch the **TestDisk** application.

TestDisk displays the log creation screen.

Three options are available:

* **Create** – Creates a new log file containing technical information and messages.
* **Append** – Adds information to an existing log file.
* **No Log** – Runs TestDisk without creating a log file.

Select **Create** and press **Enter** to create a new log file.

---

### Step 2: Select Disk

TestDisk displays all detected storage devices along with their sizes.

Use the **Up/Down Arrow keys** to select the storage device containing the missing or damaged partition.

Select the required disk and press **Enter** to proceed.

---

### Step 3: Select Partition Table Type

TestDisk displays the available partition table types.

The default partition table type is normally selected automatically because TestDisk detects the partition structure.

Select the detected/default partition table type and press **Enter**.

---

### Step 4: Analyse the Partition Structure

TestDisk displays the main menu.

Select **Analyse** to examine the current partition structure and search for lost partitions.

Press **Enter** to proceed.

The current partition structure is displayed.

The partition information is examined for:

* Missing partitions
* Duplicate partition entries
* Invalid partition entries
* File-system errors
* Corrupted partitions

The analysis showed that one partition was listed twice, indicating a possible corrupted partition or invalid partition table entry.

The message **Invalid NTFS boot** indicated that the NTFS boot sector was faulty.

---

### Step 5: Start Quick Search

Select **Quick Search** and press **Enter**.

TestDisk starts searching for lost partitions.

The search results are displayed in real time.

During the Quick Search, TestDisk detects the available partitions, including the missing logical partition.

---

### Step 6: Verify the Recovered Partition

Highlight the detected partition and press **P** to list its files.

The directories and files stored in the partition are displayed.

The contents are checked to verify whether the detected partition is the correct partition.

Files and folders can be navigated using the arrow keys.

Press **Q** to return to the previous screen.

---

### Step 7: Perform Deeper Search

If the required partition is not completely recovered using Quick Search, select **Deeper Search** and press **Enter**.

Deeper Search performs a more detailed scan of the storage device.

It searches for:

* FAT32 backup boot sectors
* NTFS backup boot sectors
* NTFS backup boot structures
* ext2/ext3 backup superblocks
* Additional lost partitions

The complete disk is scanned to identify additional missing partitions.

---

### Step 8: Examine Deeper Search Results

After the Deeper Search is completed, TestDisk displays the detected partitions.

The missing partition is identified using the backup boot sector.

The message:

**NTFS found using backup sector!**

indicates that TestDisk has detected the NTFS partition using its backup boot sector.

Some partitions may be displayed with status **D (Deleted)**.

When two partitions overlap, TestDisk may mark both as deleted until the correct partition is identified.

---

### Step 9: Verify the Damaged Partition

Highlight the first detected partition and press **P** to list its files.

The file system of this partition was found to be damaged, and the expected files were not correctly displayed.

Press **Q** to return to the partition list.

Keep the damaged partition marked as **D (Deleted)**.

---

### Step 10: Identify the Correct Partition

Highlight the second partition with the same partition label and press **P**.

TestDisk displays the files and directories stored in the partition.

The files are correctly listed, confirming that this is the correct partition.

Use the **Left/Right Arrow keys** to navigate through folders and verify the contents.

Press **Q** to return to the partition list.

---

### Step 11: Change Partition Status

TestDisk provides different partition statuses, such as:

* **P** – Primary
* ***** – Bootable
* **L** – Logical
* **D** – Deleted

The correctly identified partition was initially marked as **D (Deleted)**.

Use the **Left/Right Arrow keys** to change its status from:

**D (Deleted) → L (Logical)**

This marks the partition as a valid logical partition for recovery.

Press **Enter** to proceed.

---

### Step 12: Write the Recovered Partition Table

TestDisk displays the option to write the recovered partition structure.

Select **Write** and press **Enter**.

TestDisk asks for confirmation.

Select **Y (Yes)** to confirm the operation.

The recovered partition structure is then written to the partition table.

After successful writing, the recovered partition is registered in the partition table.

---

### Step 13: Check the NTFS Boot Sector

The NTFS boot sector of the first partition was found to be damaged.

TestDisk displays the boot sector status as:

**Bad**

The backup boot sector is found to be valid.

Therefore, the valid backup boot sector can be used to repair the damaged boot sector.

---

### Step 14: Repair the NTFS Boot Sector

Select the **Backup BS** option.

Press **Enter** to proceed.

TestDisk asks for confirmation.

Press **Y** to confirm copying the backup boot sector over the damaged boot sector.

TestDisk copies the valid backup boot sector to the main NTFS boot sector.

---

### Step 15: Verify Boot Sector Recovery

After the repair operation, TestDisk displays that the boot sector and its backup are now valid and identical.

The NTFS boot sector has been successfully recovered.

The damaged NTFS boot sector is therefore repaired using the valid backup boot sector.

Press **Enter** to continue.

---

### Step 16: Restart the Linux System

TestDisk displays the message:

**You have to restart your Computer to access your data.**

Press **Enter** and restart the Linux system.

After restarting, the recovered partition and its data can be accessed normally, provided the recovery was successful.

## Recovery Verification

| Parameter          | Result                       |
| ------------------ | ---------------------------- |
| Recovery Tool      | TestDisk                     |
| Operating System   | Linux                        |
| Operation          | Lost Partition Recovery      |
| Search Method      | Quick Search / Deeper Search |
| Partition Status   | D (Deleted) → L (Logical)    |
| File Listing       | Files successfully displayed |
| Partition Table    | Successfully recovered       |
| NTFS Boot Sector   | Repaired                     |
| Backup Boot Sector | Valid                        |
| Boot Sector Status | OK                           |
| Data Recovery      | Successful                   |

## Result

The missing/damaged partition was successfully identified and recovered using **TestDisk** on a **Linux operating system**.

The correct partition was verified by listing its files, and its status was changed from **D (Deleted)** to **L (Logical)**. The recovered partition structure was successfully written to the partition table.

The damaged NTFS boot sector was also repaired using the valid backup boot sector.

**Therefore, the deleted/missing partition was successfully recovered and the corrupted NTFS boot sector was repaired using TestDisk on a Linux operating system.**
<img width="836" height="313" alt="WhatsApp Image 2026-08-23 at 9 35 27 PM" src="https://github.com/user-attachments/assets/53b4f9d7-e1b8-46f6-ac32-9feabcc79883" />

<img width="836" height="313" alt="WhatsApp Image 2026-08-23 at 9 35 28 PM" src="https://github.com/user-attachments/assets/d3410874-0059-4d51-ad2d-fc914eed37d3" />

<img width="836" height="314" alt="WhatsApp Image 2026-08-23 at 9 35 28 PM (1) - Copy" src="https://github.com/user-attachments/assets/c88b406f-a016-48dd-ba1d-7f1e7da3582d" />

<img width="836" height="314" alt="WhatsApp Image 2026-08-23 at 9 35 29 PM" src="https://github.com/user-attachments/assets/f97b450f-276b-4850-a8de-ba4209680e91" />

<img width="836" height="314" alt="WhatsApp Image 2026-08-23 at 9 35 29 PM (1)" src="https://github.com/user-attachments/assets/17933d30-9488-4e4a-9e8c-d261d14233e5" />

<img width="836" height="314" alt="WhatsApp Image 2026-08-23 at 9 35 30 PM" src="https://github.com/user-attachments/assets/b0362af8-b2a0-4fa7-883c-70626603c07d" />
