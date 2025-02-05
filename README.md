# Workshop Malspam

**By Norwegian CERT for Health and Municipalities**<br>
**Content has been cloned from https://github.com/helsecert/workshop_malspam and re-uploaded with the permission from the owner**<br>
**Content is intended for EDUCATIONAL reasons**<br>

This workshop is a hands-on introduction to malspam investigation.

> **⚠️ Warning:** This workshop includes real malware samples. Use appropriate caution. If you're unsure what that entails, consult someone knowledgeable or research proper precautions before starting.

---

## 🛠️ Tools and Setup

### Virtual Machine

**Remnux VM** is the recommended OS for reverse engineering these samples due to already having most of the needed tools pre-installed.

### Tools Used

The following (non-exhaustive) list of tools will be used during the workshop:

- **VS Code** – For syntax highlighting and editing (included in Remnux)
- **7-Zip** - For file extraction/content extraction (git clone https://github.com/decalage2/oletools)
- **Oletools** - For analyzing OLE files. (included in Remnux) 
- **lnkinfo** – For inspecting LNK (shortcut) files. (Install through Remnux repo's: liblnk-utils)
- **Peepdf** - For analyzing and extracting information from PDF files (included in Remnux)
- **Wireshark** - Network protocol analyzer used to capture and inspect data packets (included in Remnux)
- **MSItools** - For working with MSI files, including extracting and modifying installation packages (included in Remnux)
- **Bless** - Hex editor used for editing/inspecting binary files (Install through Remnux repo's: bless)
- **Onedump.py** - Working with one-note files (Fetch from: https://github.com/DidierStevens/Beta/blob/master/onedump.py)
- **Cyberchef** - Decoding payloads etc. (https://gchq.github.io/CyberChef/)

*Note:* You may substitute these tools with alternatives, but demonstrations are based on using the above tools.

---

## 🚀 How to Use

All cases follow the same process:

1. **Unpack `stage1.7z`**  
   All Stage 1 samples are encrypted with the password `infected`. To decrypt, use:
   ```bash
   $ 7z x stage1.7z -pinfected

   Your mission (should you choose to accept it)
The goal is to investigate the file within to determine:

1 - Is it malicious? If so find:
2 - IOCs
URLS / IPs
filepaths
regkeys
other relevant IOCs to use for detection/remediation
Repeat this for all stages until you end up with either a congratulatory text-file, or a .exe/.dll.
Tips and tricks
It is advised to:

hash files before starting analysis. (keeps a clear trail, and helps detect unwanted alterations)
note steps taken, and commands run for repeatability
Follow on stages
If the folder contains a stage2.7z, og other variants they will always unpack with the downloadURL as the password. E.g. stage2.7z for putty.msi would unpack as follows: $7z x stage2.7z -phttps://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.81-installer.msi

Intended order:
demo
1_powershell
2_vbs
3_lnk
4_doc
5_excel
HTA
bat
JS
onenote
ppt
tasks
