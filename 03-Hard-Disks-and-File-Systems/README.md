<p align="center">
  <img src="./images/cover.png" alt="CHFI Module 03 cover" width="800"/>
</p>

# Module 03: Understanding Hard Disks and File Systems

### Forensic analysis of three disk images

[Back to portfolio](../README.md) · [Lab report (PDF)](./Lab-Report.pdf) · [Chain of custody (PDF)](./Chain-of-Custody.pdf)

---

## Overview

Forensic analysis of three disk images covering file system structure, deleted data recovery, timeline analysis and file signature verification. All images were integrity-verified with SHA-256 before analysis.

|                  |                                                                                  |
| ---------------- | -------------------------------------------------------------------------------- |
| **Case ID**      | `CASE-2026-M3`                                                                   |
| **Tools**        | `WinHex` `PhotoRec` `mactime`                                                    |
| **Hashes**       | SHA-256                                                                          |

## Evidence

| Item   | Image                                   | Result                                                                                  |
| ------ | --------------------------------------- | --------------------------------------------------------------------------------------- |
| EV-001 | Incomplete Ext4 image from an Ubuntu 16.04 virtual machine | Recovered `HideMarkedCols.xls`, a 2011 file found on a 2016 system          |
| EV-002 | 2 GiB NTFS volume                       | 22 deleted files recovered with timestamps, file signatures verified                    |
| EV-003 | MBR disk with two NTFS partitions       | Partition layout examined                                                               |

## Techniques

| Area                       | What was done                                                                   |
| -------------------------- | ------------------------------------------------------------------------------- |
| File system structure      | Examined Ext4, NTFS and MBR layouts                                             |
| Deleted data recovery      | Metadata-based recovery and file carving with WinHex and PhotoRec               |
| Timeline analysis          | Activity timelines built with `mactime`                                         |
| Signature verification     | File headers checked against file extensions                                    |

## Chain of Custody

The record for Labs 1 to 5 documents the three original images and the derived evidence: recovered files, carved files, timelines, signature checks and slack space. It includes the transfer log, storage locations and hash values. The images were retained for later modules.
