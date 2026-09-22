# Ex. No. 5 – Use Autopsy to Create a Case and Import Evidence

## Digital Forensics Lab

### Aim

To create a forensic case using Autopsy and import a forensic disk image as evidence for digital forensic analysis.

---

## Software Used

- Autopsy 4.23.1
- Windows
- Digital Forensic Disk Image (.E01)

---

## Case Information

| Property | Details |
|---|---|
| Case Name | laptop theft |
| Case Number | case 1 |
| Examiner | Navadeep |
| Evidence Image | 4Dell Latitude CPi.E01 |
| Timezone | Asia/Calcutta |
| Autopsy Version | 4.23.1 |

---

## Description

Autopsy is an open-source digital forensics platform used for analyzing and extracting data from digital devices.

In this experiment, a new forensic case was created in Autopsy and the forensic image `4Dell Latitude CPi.E01` was imported. Ingest modules were configured to analyze the evidence and extract forensic artifacts.

An HTML forensic report was also generated after the analysis.

---

# Procedure

## 1. Create a New Case

Autopsy was opened and a new case was created.

The case information was entered as follows:

- Case Name: `laptop theft`
- Case Number: `case-001`
- Examiner: `Rakesh`


<img width="1678" height="896" alt="Screenshot 2026-09-07 115112" src="https://github.com/user-attachments/assets/236aa8b8-ed3f-4ca4-9ad6-32fc6cd07e6d" />


## 2. Select Host

A new host was generated based on the data source name.

<img width="1907" height="988" alt="Screenshot 2026-09-07 115152" src="https://github.com/user-attachments/assets/6a9cd717-99bc-4f2d-8ca8-1f827beb3bb6" />

## 3. Select Data Source

The forensic evidence image was selected as the data source.

**Evidence:**

`4Dell Latitude CPi.E01`


## 4. Configure Ingest Modules

The required ingest modules were configured for forensic analysis.

The selected modules included:

- Recent Activity
- Hash Lookup
- File Type Identification
- Extension Mismatch Detector
- Embedded File Extractor
- Picture Analyzer
- Email Parser
- Encryption Detection
- Interesting Files Identifier
- Central Repository
- PhotoRec Carver
- Virtual Machine Extractor


## 5. Analyze Evidence

After the evidence was added, Autopsy processed the forensic image using the configured ingest modules.

The results were displayed in the Autopsy interface.



<img width="1253" height="807" alt="Screenshot 2026-09-07 115324" src="https://github.com/user-attachments/assets/ace1021a-fe8c-4d50-b928-e90cace6ffd9" />


## 6. Generate Report

After the analysis was completed, the **Generate Report** option was selected.

The **HTML Report** module was selected to generate the forensic report.



<img width="1053" height="652" alt="Screenshot 2026-09-07 115349" src="https://github.com/user-attachments/assets/a16563e3-72b9-457d-8e45-c9ecfb79b8c6" />


## 7. View Generated Report

Autopsy generated an HTML forensic report containing information about the case and analyzed evidence.



## 8. Report Generation Completed

The report generation process was completed successfully and the HTML report was saved in the Reports directory.

<img width="1918" height="1015" alt="Screenshot 2026-09-07 115712" src="https://github.com/user-attachments/assets/79e8d0f3-7f79-4b02-ac60-20a5c12b2e0a" />


<img width="1107" height="765" alt="Screenshot 2026-09-07 115744" src="https://github.com/user-attachments/assets/dd96b192-dde0-461d-9495-3760ca2c8b66" />


<img width="988" height="613" alt="Screenshot 2026-09-07 115809" src="https://github.com/user-attachments/assets/50cd6c61-d813-408a-ad24-89fc7b272514" />


<img width="1855" height="905" alt="Screenshot 2026-09-07 115835" src="https://github.com/user-attachments/assets/7bd1fdcc-235f-4ec4-99ef-20c9989c5828" />


# Evidence Information

| Property | Details |
|---|---|
| Case Name | laptop theft |
| Case Number | case 1 |
| Examiner | Navadeep |
| Data Source | 4Dell Latitude CPi.E01 |
| Sector Size | 512 Bytes |
| Timezone | Asia/Calcutta |
| Autopsy Version | 4.23.1 |

---

# Analysis Performed

The forensic image was analyzed using Autopsy ingest modules.

The analysis included:

- File Type Identification
- Hash Lookup
- Extension Mismatch Detection
- Embedded File Extraction
- Picture Analysis
- Email Parsing
- Encryption Detection
- Interesting Files Identification
- Recent Activity Analysis
- File Carving

---

# Result

The forensic disk image was successfully imported into Autopsy and analyzed using the configured ingest modules.

Various forensic artifacts were extracted and categorized by Autopsy.

An HTML forensic report was successfully generated containing the case and analysis information.


<img width="1565" height="906" alt="Screenshot 2026-09-07 115850" src="https://github.com/user-attachments/assets/7fe40ab0-5f4a-4167-a6cc-fc4cbd7e4c6b" />


# Conclusion

The experiment successfully demonstrated how to create a forensic case in Autopsy, import a forensic disk image, configure ingest modules, analyze the evidence, and generate an HTML forensic report.

<img width="1565" height="906" alt="Screenshot 2026-09-07 115850" src="https://github.com/user-attachments/assets/1f6b377f-a406-411a-9ba9-9cacf0f65c3e" />


# Experiment Workflow

```text
Create New Case
       ↓
Enter Case Information
       ↓
Select Host
       ↓
Select Data Source
       ↓
Import 4Dell Latitude CPi.E01
       ↓
Configure Ingest Modules
       ↓
Analyze Evidence
       ↓
Generate HTML Report
       ↓
Review Report
       ↓
Complete
