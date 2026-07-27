<div align="center">

# 🔍 Digital Forensic Examination of a USB Flash Drive

### A Digital Forensics Investigation Using The Sleuth Kit (TSK) on SIFT Workstation

*Preserving Evidence • Recovering Digital Artifacts • Maintaining Forensic Integrity*

</div>

---

## 📖 Project Overview

This repository documents a digital forensic examination of a USB flash drive image (`flash.dd`) using **The Sleuth Kit (TSK)** on the **SANS Investigative Forensic Toolkit (SIFT) Workstation**.

The investigation was conducted using accepted digital forensic principles to ensure the integrity of the original evidence while identifying and recovering relevant digital artifacts.

---

## 🎯 Investigation Objectives

- Verify the forensic image
- Examine the partition layout
- Identify the file system
- Enumerate files within the image
- Recover digital evidence
- Identify deleted files
- Document forensic findings

---

## 🛠️ Investigation Environment

| Component | Details |
|-----------|---------|
| Operating System | SIFT Workstation |
| Tool Suite | The Sleuth Kit (TSK) |
| Evidence Image | `flash.dd` |
| Partition Table | DOS (MBR) |
| File System | FAT32 |
| Volume Label | OTG ORG |
| Offset | 64 |

---

# 🔬 Investigation Workflow

```text
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
```

---

# 💻 Commands Executed

```bash
img_stat flash.dd

mmls flash.dd

fsstat -o 64 flash.dd

fls -o 64 flash.dd

icat -o 64 flash.dd 52 > ts119a.exe

fls -r -d -o 64 flash.dd
```

---

# 📂 Digital Evidence

## 📌 Figure 1 — Image Verification

<p align="center">
  <img src="evidence/Screenshot%202026-07-27%20114255.png" width="900">
</p>

---

## 📌 Figure 2 — Partition Analysis

<p align="center">
  <img src="evidence/Screenshot%202026-07-27%20113557.png" width="900">
</p>

---

## 📌 Figure 3 — File System Analysis

<p align="center">
  <img src="evidence/Screenshot%202026-07-27%20113746.png" width="900">
</p>

---

## 📌 Figure 4 — File Enumeration

<p align="center">
  <img src="evidence/Screenshot%202026-07-27%20113909.png" width="900">
</p>

---

## 📌 Figure 5 — Evidence Recovery

<p align="center">
  <img src="evidence/Screenshot%202026-07-27%20114137.png" width="900">
</p>

---

## 📌 Figure 6 — Deleted File Analysis

<p align="center">
  <img src="evidence/Screenshot%202026-07-27%20114035.png" width="900">
</p>
---

# 📊 Key Findings

| Examination Item | Result |
|------------------|--------|
| Image Type | Raw (.dd) |
| Partition Table | DOS (MBR) |
| Partition Offset | 64 |
| File System | FAT32 |
| Volume Label | OTG ORG |
| Recovered File | ts119a.exe |
| Deleted Files | Successfully Identified |

---

# 📁 Repository Structure

```text
digital-forensic-usb-examination/
│
├── README.md
│
├── report/
│   └── Digital_Forensic_Examination_Report.pdf
│
├── evidence/
│   ├── 01_img_stat.png
│   ├── 02_mmls.png
│   ├── 03_fsstat.png
│   ├── 04_fls.png
│   ├── 05_icat.png
│   └── 06_deleted_files.png
│
└── assets/
```

---

# 🧠 Skills Demonstrated

- Digital Forensic Investigation
- Evidence Preservation
- USB Storage Device Analysis
- FAT32 File System Analysis
- Deleted File Identification
- File Recovery
- Linux Command Line
- The Sleuth Kit (TSK)
- SIFT Workstation
- Technical Report Writing

---

# ✅ Conclusion

This project demonstrates a structured digital forensic examination of a USB flash drive image using industry-standard forensic tools and methodology. The investigation verified the forensic image, analyzed the partition structure and FAT32 file system, identified stored files, recovered digital evidence, and examined deleted file artifacts while preserving the integrity of the original evidence.

---

# 📌 Disclaimer

This repository was created for educational and laboratory purposes. All analysis was performed on a forensic image in a controlled environment. The repository is intended to demonstrate digital forensic techniques and documentation practices.

---

<div align="center">

### ⭐ Thank you for visiting this repository.

**Feedback and suggestions are always welcome.**

</div>
