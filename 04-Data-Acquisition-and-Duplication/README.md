<div align="center">

<img src="./images/cover4.png" alt="CHFI Module 04 — Data Acquisition and Duplication" width="100%" />

<br><br>

<h1>Module 04 — Data Acquisition and Duplication</h1>
<h3>The Full Acquisition Pipeline, from Live Memory to Forensic Images</h3>

<br>

<img src="https://img.shields.io/badge/MODULE-04-0d1117?style=for-the-badge&labelColor=0d1117&color=00b4d8" />
<img src="https://img.shields.io/badge/STATUS-COMPLETED-0d1117?style=for-the-badge&labelColor=0d1117&color=00b4d8" />
<img src="https://img.shields.io/badge/LABS-7-0d1117?style=for-the-badge&labelColor=0d1117&color=00b4d8" />
<img src="https://img.shields.io/badge/IMAGES-WINDOWS%20%2B%20MAC%20HFS%2B-0d1117?style=for-the-badge&labelColor=0d1117&color=00b4d8" />

<br><br>

<a href="#lab-walkthrough"><b>Labs</b></a> &nbsp;·&nbsp;
<a href="#principles-applied"><b>Principles</b></a> &nbsp;·&nbsp;
<a href="#key-takeaways"><b>Takeaways</b></a> &nbsp;·&nbsp;
<a href="#lab-environment"><b>Environment</b></a> &nbsp;·&nbsp;
<a href="#full-report"><b>Full Report</b></a>

</div>

<br>

---

## Executive Summary

This module documents hands-on labs covering the complete acquisition pipeline: imaging disks, converting and mounting images, capturing RAM and reading images through scripts. The tools used were **dd, xmount, FTK Imager, DiskExplorer, Belkasoft, fmem, LiME, netcat and pytsk3**, on both Windows images and Mac HFS+ images.

The labs follow the order of volatility, verify images with hashes and never modify the original evidence.

> All work was performed on lab evidence for educational purposes.

<br>

## Lab Walkthrough

<table>
<tr><th>Lab</th><th>What Was Done</th><th>Tool</th></tr>
<tr><td><b>Disk Imaging</b></td><td>Imaging with <code>dd</code> on Windows</td><td><code>dd</code></td></tr>
<tr><td><b>Image Conversion</b></td><td>E01 to raw conversion</td><td><code>xmount</code></td></tr>
<tr><td><b>Read-Only Mounting</b></td><td>Windows and Mac HFS+ images mounted read-only</td><td><code>xmount</code></td></tr>
<tr><td><b>RAM Acquisition</b></td><td>Memory captured with four different tools</td><td><code>Belkasoft</code> <code>fmem</code> <code>LiME</code> <code>netcat</code></td></tr>
<tr><td><b>Custom Imaging</b></td><td>Disk image created with DiskExplorer</td><td><code>DiskExplorer</code></td></tr>
<tr><td><b>Image Viewing</b></td><td>Images opened and browsed</td><td><code>FTK Imager</code></td></tr>
<tr><td><b>Scripted Access</b></td><td>Image contents read with Python</td><td><code>pytsk3</code></td></tr>
</table>

**Pipeline:** capture volatile memory first → image the disk → convert the format → mount read-only → inspect with GUI tools and scripts.

<br>

## Principles Applied

<table>
<tr><th>Principle</th><th>Meaning</th></tr>
<tr><td><b>Order of Volatility</b></td><td>Capture the most volatile data first</td></tr>
<tr><td><b>Hashing</b></td><td>Verify every image against the source</td></tr>
<tr><td><b>Original Evidence Intact</b></td><td>Work on images and mount them read-only</td></tr>
</table>

<br>

## Key Takeaways

- **Acquisition order matters.** RAM disappears when a machine powers off, so it is captured before disk imaging.
- **Verification is mandatory.** An image is only useful if its hash matches the source.
- **Read-only mounting protects evidence.** Both Windows and Mac HFS+ images were examined without altering them.
- **Scripts scale analysis.** Reading images with Python and `pytsk3` makes the same work repeatable.

<br>

## Lab Environment

| | |
|---|---|
| **Image Types** | Windows images and Mac HFS+ images |
| **Tools Used** | `dd` `xmount` `FTK Imager` `DiskExplorer` `Belkasoft` `fmem` `LiME` `netcat` `pytsk3` |
| **Published Material** | Report only |

<br>

## Full Report

The complete lab report is available here:

📄 **[Lab-Report.pdf](./Lab-Report.pdf)**

<br>

## Disclaimer

This work was carried out for educational purposes under the EC-Council CHFI curriculum. Disk images and memory dumps are not published in this repository.

<br>

<div align="center">

⬅ <a href="../"><b>Back to Main Repository</b></a>

</div>
