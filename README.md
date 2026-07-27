# Digital Forensic Examination of a USB Flash Drive Image

## Overview

This repository documents a digital forensic examination of a USB flash drive image (`flash.dd`) using **The Sleuth Kit (TSK)** on the **SANS Investigative Forensic Toolkit (SIFT) Workstation**.

The objective of this examination was to analyze a forensic image while preserving the integrity of the original evidence. The investigation included image verification, partition analysis, file system identification, file enumeration, file recovery, and deleted file analysis.

---

## Objectives

- Verify the forensic image.
- Identify the partition layout.
- Determine the file system.
- List files stored within the image.
- Recover a selected file.
- Identify deleted files.

---

## Investigation Environment

| Component | Details |
|-----------|---------|
| Operating System | SIFT Workstation |
| Tool Suite | The Sleuth Kit (TSK) |
| Evidence Image | flash.dd |
| File System | FAT32 |
| Partition Type | DOS (MBR) |
| Start Sector | 64 |

---

## Tools Used

- SIFT Workstation
- The Sleuth Kit (TSK)
- Linux Terminal
- img_stat
- mmls
- fsstat
- fls
- icat

---

## Methodology

The forensic examination followed these stages:

1. Image Verification
2. Partition Identification
3. File System Analysis
4. File Enumeration
5. File Recovery
6. Deleted File Analysis

The analysis was conducted on the forensic image instead of the original USB device to maintain evidence integrity.

---

# Commands Used

```bash
img_stat flash.dd

mmls flash.dd

fsstat -o 64 flash.dd

fls -o 64 flash.dd

icat -o 64 flash.dd 52 > ts119a.exe

fls -r -d -o 64 flash.dd
```

---

# Evidence

## Figure 1 – Image Verification

![img_stat](evidence/01_img_stat.png)

---

## Figure 2 – Partition Analysis

![mmls](evidence/02_mmls.png)

---

## Figure 3 – File System Analysis

![fsstat](evidence/03_fsstat.png)

---

## Figure 4 – File Listing

![fls](evidence/04_fls.png)

---

## Figure 5 – File Recovery

![icat](evidence/05_icat.png)

---

## Figure 6 – Deleted File Analysis

![deleted files](evidence/06_deleted_files.png)

---

## Key Findings

| Finding | Result |
|----------|--------|
| Image Format | Raw (.dd) |
| Partition Table | DOS (MBR) |
| File System | FAT32 |
| Volume Label | OTG ORG |
| Start Sector | 64 |
| Recovered File | ts119a.exe |

---

## Repository Structure

```text
digital-forensic-usb-examination
│── README.md
│
├── report
│   └── Digital_Forensic_Examination_Report.pdf
│
├── evidence
│   ├── 01_img_stat.png
│   ├── 02_mmls.png
│   ├── 03_fsstat.png
│   ├── 04_fls.png
│   ├── 05_icat.png
│   └── 06_deleted_files.png
```

---

## Conclusion

The forensic examination successfully verified the forensic image, identified the partition layout and FAT32 file system, enumerated stored files, recovered a selected executable file, and identified deleted file entries. The investigation demonstrates the practical application of The Sleuth Kit (TSK) for digital forensic analysis while maintaining the integrity of digital evidence.

---

## Disclaimer

This repository was created for educational and laboratory purposes. All analysis was conducted on a forensic image within a controlled environment.
