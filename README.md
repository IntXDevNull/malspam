# Workshop Malspam

**By Norwegian CERT for Health and Municipalities**

This workshop is a hands-on introduction to malspam investigation.

> **⚠️ Warning:** This workshop includes real malware samples. Use appropriate caution. If you're unsure what that entails, consult someone knowledgeable or research proper precautions before starting.

---

## 🛠️ Tools and Setup

### Virtual Machine

The demonstrations in this workshop are based on a **Remnux VM**. Using a virtual machine (VM) is best practice when analyzing anything malicious. Remnux is lightweight and comes preloaded with many useful tools for malware analysis.

### Tools Used

The following (non-exhaustive) list of tools will be used during the workshop:

- **VS Code** – For syntax highlighting and editing
- **7-Zip** (included in Remnux) – For file extraction
- **Oletols** (included in Remnux) – For analyzing OLE files
- **lnkinfo** – For inspecting LNK (shortcut) files

*Note:* You may substitute these tools with alternatives, but demonstrations are based on using the above tools.

---

## 🚀 How to Use

All cases follow the same process:

1. **Unpack `stage1.7z`**  
   All Stage 1 samples are encrypted with the password `infected`. To decrypt, use:
   ```bash
   $ 7z x stage1.7z -pinfected
