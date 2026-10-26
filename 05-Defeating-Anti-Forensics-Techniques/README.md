<p align="center">
  <img src="./images/cover.png" alt="CHFI Module 05 cover" width="800"/>
</p>

# Module 05: Defeating Anti-Forensics Techniques

### Identifying and countering techniques used to hide or destroy evidence

[Back to portfolio](../README.md) · [Lab report (PDF)](./Lab-Report.pdf)

---

## Overview

Eight practical labs on deliberate anti-forensic techniques and the methods used to detect or defeat them. All analysis was read-only, and recovered or decrypted artifacts were written to separate export folders so the original evidence stayed unmodified.

|                  |                                                                                                                      |
| ---------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Labs**         | 8                                                                                                                    |
| **Tools**        | `R-Studio` `pwdump7` `Passware Kit Forensic` `Advanced Archive Password Recovery` `Advanced PDF Password Recovery` `StegSpy` `OpenStego` `zsteg` `DeepSound` `Autopsy` `Detect It Easy` `Exeinfo PE` |

## Labs

| #  | Technique                         | Result                                                                                                  |
| -- | --------------------------------- | ------------------------------------------------------------------------------------------------------- |
| 1  | SSD TRIM anti-carving (Windows)   | TRIM enabled: no recoverable files. TRIM disabled: deleted files (a GIF and a text file) carved successfully |
| 2  | SSD TRIM anti-carving (Linux)     | Same behaviour confirmed, with TRIM off the deleted files were recovered                                |
| 3  | Partition deletion and merge concealment | Deleted partition fully recovered with an R-Studio detailed sector scan, including `Infected.exe` and `Confidential.pdf` |
| 4  | Credential extraction             | `pwdump7` extracted LM and NTLM hashes from the live SAM database                                       |
| 5  | Application password cracking     | Password-protected PDF, RAR and Word files opened with Passware Kit Forensic, Advanced Archive Password Recovery and Advanced PDF Password Recovery |
| 6  | Steganography detection           | Hidden data found and extracted from images (StegSpy, OpenStego, zsteg) and audio (DeepSound)           |
| 7  | File extension mismatch           | Autopsy's Extension Mismatch Detector found files whose content did not match their extension, such as a JPEG disguised as `.trace` |
| 8  | Executable packing                | Detect It Easy and Exeinfo PE identified packing and obfuscation on `Infected.exe`                      |

## Key Takeaway

Anti-forensic techniques mostly change metadata, structure or surface appearance. The countermeasure is to inspect the underlying bytes (file signatures, entropy, raw sectors) and not to trust file names, extensions or the live partition table.
