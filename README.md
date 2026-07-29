# Digital Forensic Examination of a USB Flash Drive

### A Digital Forensics Investigation Using The Sleuth Kit (TSK) on SIFT Workstation

![Linux](https://img.shields.io/badge/Linux-SIFT_Workstation-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![TSK](https://img.shields.io/badge/The_Sleuth_Kit-Forensics-0052CC?style=for-the-badge)
![File System](https://img.shields.io/badge/File_System-FAT32-2EA44F?style=for-the-badge)
![Image Type](https://img.shields.io/badge/Image-Raw_.dd-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

## Project Overview

This repository documents a digital forensic examination of a USB flash drive image (`flash.dd`) using **The Sleuth Kit (TSK)** on the **SANS Investigative Forensic Toolkit (SIFT) Workstation**.

The investigation was conducted using accepted digital forensic principles to ensure the integrity of the original evidence while identifying and recovering relevant digital artifacts.



## Investigation Objectives

- Verify the forensic image
- Examine the partition layout
- Identify the file system
- Enumerate files within the image
- Recover digital evidence
- Identify deleted files
- Document forensic findings


## Investigation Environment

| Component | Details |
|-----------|---------|
| Operating System | SIFT Workstation |
| Tool Suite | The Sleuth Kit (TSK) |
| Evidence Image | `flash.dd` |
| Partition Table | DOS (MBR) |
| File System | FAT32 |
| Volume Label | OTG ORG |
| Offset | 64 |



# Investigation Workflow


USB Flash Drive
        │
        ▼
Forensic Image Acquisition
        │
        ▼
Image Verification
        │
        ▼
Partition Analysis
        │
        ▼
File System Identification
        │
        ▼
File Enumeration
        │
        ▼
Evidence Recovery
        │
        ▼
Deleted File Analysis
        │
        ▼
Digital Forensic Findings


#  Commands Executed
bash
img_stat flash.dd

mmls flash.dd

fsstat -o 64 flash.dd

fls -o 64 flash.dd

icat -o 64 flash.dd 52 > ts119a.exe

fls -r -d -o 64 flash.dd


# Digital Evidence

## Figure 1 — Image Verification

<p align="center">
  <img src="./evidence/Screenshot%202026-07-27%20114255.png" alt="Image Verification" width="900">
</p>

**Figure 1.** Verification of the forensic image using the `img_stat` command.

---

## Figure 2 — Partition Analysis

<p align="center">
  <img src="./evidence/Screenshot%202026-07-27%20113557.png" alt="Partition Analysis" width="900">
</p>

**Figure 2.** Identification of the DOS (MBR) partition table and partition offset using `mmls`.

---

## Figure 3 — File System Analysis

<p align="center">
  <img src="./evidence/Screenshot%202026-07-27%20113746.png" alt="File System Analysis" width="900">
</p>

**Figure 3.** Examination of the FAT32 file system and volume information using `fsstat`.

---

## Figure 4 — File Enumeration

<p align="center">
  <img src="./evidence/Screenshot%202026-07-27%20113909.png" alt="File Enumeration" width="900">
</p>

**Figure 4.** Listing of files and directories stored within the forensic image using `fls`.

---

## Figure 5 — Evidence Recovery

<p align="center">
  <img src="./evidence/Screenshot%202026-07-27%20114137.png" alt="Evidence Recovery" width="900">
</p>

**Figure 5.** Recovery of `ts119a.exe` from the forensic image using the `icat` command.

---

## Figure 5.1 — Recovered File Listing

<p align="center">
  <img src="./evidence/Screenshot%202026-07-27%20114215.png" alt="Recovered File Listing" width="900">
</p>

**Figure 5.1.** Directory listing confirming the successful recovery of `ts119a.exe`.

---

## Figure 6 — Deleted File Analysis

<p align="center">
  <img src="./evidence/Screenshot%202026-07-27%20114035.png" alt="Deleted File Analysis" width="900">
</p>

**Figure 6.** Deleted file entries identified using `fls -r -d -o 64 flash.dd`.

---

#  Key Findings

| Examination Item | Result |
|------------------|--------|
| Image Type | Raw (.dd) |
| Partition Table | DOS (MBR) |
| Partition Offset | 64 |
| File System | FAT32 |
| Volume Label | OTG ORG |
| Recovered File | `ts119a.exe` |
| Deleted Files | Successfully Identified |

---

#  Skills Demonstrated

- Digital Forensic Investigation
- Evidence Preservation and Handling
- USB Storage Device Analysis
- FAT32 File System Analysis
- Partition Analysis
- File Enumeration
- Deleted File Identification
- Digital Evidence Recovery
- Linux Command-Line Forensics
- The Sleuth Kit (TSK)
- SIFT Workstation
- Technical Report Writing

---

# Conclusion

This project demonstrates a structured digital forensic examination of a USB flash drive image using **The Sleuth Kit (TSK)** on a **SIFT Workstation**. The investigation successfully verified the forensic image, identified the partition structure and FAT32 file system, enumerated stored files, recovered digital evidence, and identified deleted file entries while maintaining the integrity of the original evidence throughout the examination process.

---

# Disclaimer

This repository was created for educational and laboratory purposes only. All forensic analysis was performed on a controlled forensic image in a virtual laboratory environment. The project is intended solely to demonstrate digital forensic investigation techniques, evidence handling, and professional documentation practices.



<div align="center">

### ⭐ Thank you for visiting this repository!

If you found this project useful, consider giving it a ⭐ on GitHub.

Feedback and suggestions are always welcome.

</div>
