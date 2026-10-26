<div align="center">

<img src="./images/cover3.png" alt="CHFI Module 03 — Understanding Hard Disks and File Systems" width="100%" />

<br><br>

<h1>Module 03 — Understanding Hard Disks and File Systems</h1>
<h3>Forensic Analysis of Three Disk Images: Ext4, NTFS and MBR</h3>

<br>

<img src="https://img.shields.io/badge/MODULE-03-0d1117?style=for-the-badge&labelColor=0d1117&color=00b4d8" />
<img src="https://img.shields.io/badge/STATUS-COMPLETED-0d1117?style=for-the-badge&labelColor=0d1117&color=00b4d8" />
<img src="https://img.shields.io/badge/EVIDENCE-3%20IMAGES-0d1117?style=for-the-badge&labelColor=0d1117&color=00b4d8" />
<img src="https://img.shields.io/badge/CHAIN%20OF%20CUSTODY-INCLUDED-0d1117?style=for-the-badge&labelColor=0d1117&color=00b4d8" />

<br><br>

<a href="#evidence"><b>Evidence</b></a> &nbsp;·&nbsp;
<a href="#techniques"><b>Techniques</b></a> &nbsp;·&nbsp;
<a href="#chain-of-custody"><b>Chain of Custody</b></a> &nbsp;·&nbsp;
<a href="#key-takeaways"><b>Takeaways</b></a> &nbsp;·&nbsp;
<a href="#full-report"><b>Full Report</b></a>

</div>

<br>

---

## Executive Summary

This module documents the forensic analysis of three disk images covering **file system structure, deleted data recovery, timeline analysis and file signature verification**. The work used **WinHex, PhotoRec and mactime** across Ext4, NTFS and MBR layouts.

All images were integrity-verified with SHA-256 before analysis began.

> All work was performed on lab evidence for educational purposes under case ID `CASE-2026-M3`.

<br>

## Evidence

<table>
<tr><th>Item</th><th>Image</th><th>Result</th></tr>
<tr><td><b>EV-001</b></td><td>Incomplete Ext4 image from an Ubuntu 16.04 virtual machine</td><td>Recovered <code>HideMarkedCols.xls</code>, a 2011 file found on a 2016 system</td></tr>
<tr><td><b>EV-002</b></td><td>2 GiB NTFS volume</td><td>22 deleted files recovered with timestamps; file signatures verified</td></tr>
<tr><td><b>EV-003</b></td><td>MBR disk with two NTFS partitions</td><td>Partition layout examined</td></tr>
</table>

<br>

## Techniques

<table>
<tr><th>Area</th><th>What Was Done</th><th>Tool</th></tr>
<tr><td><b>File System Structure</b></td><td>Examined Ext4, NTFS and MBR layouts</td><td><code>WinHex</code></td></tr>
<tr><td><b>Deleted Data Recovery</b></td><td>Metadata-based recovery and file carving</td><td><code>WinHex</code> <code>PhotoRec</code></td></tr>
<tr><td><b>Timeline Analysis</b></td><td>Activity timelines built from file system timestamps</td><td><code>mactime</code></td></tr>
<tr><td><b>Signature Verification</b></td><td>File headers checked against file extensions</td><td><code>WinHex</code></td></tr>
</table>

<br>

## Chain of Custody

The record for Labs 1 to 5 documents the three original images and the derived evidence.

<table>
<tr><th>Item</th><th>Detail</th></tr>
<tr><td><b>Original Evidence</b></td><td>EV-001, EV-002 and EV-003 disk images</td></tr>
<tr><td><b>Derived Evidence</b></td><td>Recovered files, carved files, timelines, signature checks and slack space</td></tr>
<tr><td><b>Records</b></td><td>Transfer log, storage locations and hash values</td></tr>
<tr><td><b>Final Disposition</b></td><td>Images retained for later modules</td></tr>
</table>

<br>

## Key Takeaways

- **Verify before you analyse.** SHA-256 hashing of every image confirms the evidence is intact before any work starts.
- **Deleted does not mean gone.** Metadata-based recovery and carving brought back 22 deleted files from the NTFS volume.
- **Timestamps tell a story.** A 2011 file on a 2016 system, and timelines built with `mactime`, show how dates support an investigation.
- **Extensions can be wrong.** Checking file headers against extensions is a basic integrity check on any recovered file.

<br>

## Lab Environment

| | |
|---|---|
| **Case ID** | `CASE-2026-M3` |
| **Tools Used** | `WinHex` `PhotoRec` `mactime` |
| **Hashes** | SHA-256 |
| **Published Material** | Reports only |

<br>

## Full Report

The lab report and the chain of custody record are available here:

📄 **[Lab-Report.pdf](./Lab-Report.pdf)**
📄 **[Chain-of-Custody.pdf](./Chain-of-Custody.pdf)**

<br>

## Disclaimer

This work was carried out for educational purposes under the EC-Council CHFI curriculum. Disk images and recovered files are not published in this repository.

<br>

<div align="center">

⬅ <a href="../"><b>Back to Main Repository</b></a>

</div>
