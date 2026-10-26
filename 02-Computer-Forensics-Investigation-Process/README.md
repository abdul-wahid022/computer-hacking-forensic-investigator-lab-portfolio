<p align="center">
  <img src="./images/cover.png" alt="CHFI Module 02 cover" width="800"/>
</p>

# Module 02: Computer Forensics Investigation Process

### Recovery, hashing and imaging of a formatted USB drive across six labs

[Back to portfolio](../README.md) · [Lab report (PDF)](./Lab-Report.pdf) · [Chain of custody (PDF)](./Chain-of-Custody.pdf)

---

## Overview

A complete forensic investigation of a formatted 32 GB Samsung USB drive, from recovery and hashing through analysis to a verified forensic image. Chain of custody was maintained throughout and the original media was never modified.

|                  |                                                                                  |
| ---------------- | -------------------------------------------------------------------------------- |
| **Subject**      | Formatted 32 GB Samsung USB drive                                                |
| **Case ID**      | `CHFI_Module2_Lab1to5_Case001`                                                   |
| **Tools**        | `EaseUS` `Autopsy` `HxD` `ExifTool` `FTK Imager` `VirusTotal`                    |
| **Hashes**       | MD5, SHA-1, SHA-256, SHA-512                                                     |

## Labs

| Lab    | Focus                                  | Result                                                                                     |
| ------ | -------------------------------------- | ------------------------------------------------------------------------------------------ |
| 1      | Data recovery                          | About 2 GB of files recovered with EaseUS                                                  |
| 2      | Hashing and malware check              | Files hashed with four algorithms, `Infected.pdf` flagged as a trojan by 44 of 62 VirusTotal engines |
| 3      | File integrity                         | Integrity demonstrated with hash comparison                                                |
| 4      | Deep analysis                          | Autopsy, HxD, ExifTool and related tools, 5 critical findings                              |
| 5 to 6 | FTK Imager evidence handling and imaging | Evidence handled in FTK Imager and a verified E01 forensic image created                 |

## Chain of Custody

The evidence record for Labs 1 to 5 covers the following.

| Item                  | Detail                                                              |
| --------------------- | ------------------------------------------------------------------- |
| Evidence              | EV-001 original USB drive, EV-002 recovered files                   |
| Derived items         | Working copies, FTK source and exported evidence                    |
| Records               | Transfer log, storage locations and access controls                 |
| Verification          | Hash values recorded with MD5 and SHA-256                           |
| Final disposition     | Retained for Lab 6 imaging                                          |
