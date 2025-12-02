# AutoPilot Hardware Hash Collection

> A streamlined batch script for collecting Windows AutoPilot hardware hashes during OOBE with automatic USB backup and serial number tracking.

## 🚀 Overview

Production-ready tool for IT professionals to collect Windows AutoPilot hardware hashes during OOBE. Automates the entire process including tool downloads, hardware collection, and organized USB backups with serial number tracking.

## ✨ Key Features

- ✅ **Zero Configuration** - Auto-installs all dependencies (NuGet, Get-WindowsAutopilotInfo)
- ✅ **Auto-Elevation** - Automatically requests administrator privileges via UAC
- ✅ **Serial Number Detection** - Automatically appends device serial numbers to filenames
- ✅ **Dual Backup** - Saves to both local drive (`C:\HWID`) and USB drive with organized folders
- ✅ **Clean Output** - Professional, color-coded interface with minimal clutter
- ✅ **OOBE-Friendly** - Designed for use during Windows setup (Shift+F10)
- ✅ **USB Auto-Backup** - Creates organized folders per device on USB drives
- ✅ **Internet Required** - Downloads latest collection tools from PowerShell Gallery

## 📦 What's Included

- **AutoPilotHWID-Collection.bat** - Main collection script
- **README-AutoPilot.md** - Complete usage documentation
- **README-AutoPilot.txt** - Plain text instructions for printing
- **AutoPilotHWID-Collection-SourceCode.txt** - Source code for easy copying

## 🔧 Requirements

- Windows 10/11 (OOBE or any Windows environment)
- Internet connection (for downloading collection tools)
- USB drive (optional, for automatic backup)
- Administrator privileges (script auto-elevates)

## 📋 Quick Start

1. **Copy script to USB drive**
2. **During Windows OOBE:** Press `Shift + F10`
3. **Run:** `d:` → `Auto` + `Tab` → `Enter`
4. **Wait 1-2 minutes** for collection
5. **Upload CSV** to Intune portal

See [README-AutoPilot.md](README-AutoPilot.md) for complete instructions.

## 📂 Output Structure

```
Local:  C:\HWID\AutoPilotHWID_[SerialNumber].csv
USB:    D:\AutoPilot_[SerialNumber]\AutoPilotHWID_[SerialNumber].csv
```

**Example:**
```
D:\AutoPilot_MZ00EERC\AutoPilotHWID_MZ00EERC.csv
```

## 🎬 How It Works

1. Auto-elevates to administrator privileges
2. Creates workspace directory
3. Retrieves device serial number from BIOS
4. Installs NuGet provider from PowerShell Gallery
5. Downloads Get-WindowsAutopilotInfo script
6. Collects hardware hash and device information
7. Saves CSV with serial number in filename
8. Backs up to USB drive in organized folder
9. Opens folder for easy access

## 🛠️ Technical Details

- **Language:** Batch Script (CMD)
- **Dependencies:** PowerShell 5.1+, NuGet, Get-WindowsAutopilotInfo
- **Execution Policy:** Bypass (auto-configured)
- **Scope:** System-wide installation (AllUsers)
- **Silent Mode:** Warnings and verbose output suppressed

## 📖 Documentation

- **Method 1:** Direct CMD (standard OOBE usage)
- **Method 2:** Run Dialog (keyboard issues workaround)
- **Method 3:** Explorer (mouse-only alternative)
- **Troubleshooting:** Common issues and solutions
- **Next Steps:** Upload instructions for Intune portal

## 🤝 Contributing

Contributions welcome! Please:
- Test on physical hardware and VMs
- Document any OOBE edge cases
- Submit issues for bugs or feature requests
- Include device models and Windows versions in reports

## 🙏 Acknowledgments

- Built using Microsoft's [Get-WindowsAutopilotInfo](https://www.powershellgallery.com/packages/Get-WindowsAutopilotInfo/) script
- Designed for Microsoft Intune Windows Autopilot deployment


**Made with ❤️ for IT Professionals**
