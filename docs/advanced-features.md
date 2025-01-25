# Advanced Windows Terminal Features 🚀

## 🎯 Learning Objectives
By the end of this guide, you'll:
- Master multi-tab and multi-pane workflows
- Integrate Windows Subsystem for Linux (WSL)
- Customize PowerShell profiles
- Configure advanced terminal settings
- Understand SSH and remote connections

## 🖥️ Tabs and Panes Mastery

### 📂 Tab Management
```bash
# Keyboard Shortcuts
Ctrl + Shift + T   # New tab
Ctrl + Shift + D   # Duplicate tab
Ctrl + Tab         # Switch tabs
Ctrl + Alt + Num   # Switch to specific tab
```

### 🔲 Pane Layouts
```
┌─────────┬─────────┐
│         │         │
│  Pane1  │  Pane2  │
│         │         │
├─────────┴─────────┤
│      Pane3        │
└─────────────────┘
```

#### Pane Navigation
```bash
Alt + Shift + -    # Split horizontally
Alt + Shift + +    # Split vertically
Alt + Arrow        # Navigate between panes
Ctrl + Shift + W   # Close pane
```

## 🐧 WSL Integration Masterclass

### 🚀 WSL Setup Challenge
1. Enable WSL:
```powershell
# Run in elevated PowerShell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

2. Install Linux Distribution
   - Open Microsoft Store
   - Search and install Ubuntu or your preferred distribution

3. Configure WSL Profile
```json
{
    "profiles": {
        "list": [
            {
                "name": "Ubuntu",
                "source": "Windows.Terminal.Wsl"
            }
        ]
    }
}
```

### 🌟 WSL Pro Features
- Seamless path translation
- Integrated file system
- Clipboard synchronization
- GPU acceleration (WSL 2)

## 🔧 PowerShell Power User Techniques

### 📝 Profile Customization
```powershell
# Create/Edit PowerShell Profile
Test-Path $PROFILE      # Check if exists
New-Item -Path $PROFILE -Type File -Force
notepad $PROFILE        # Open for editing
```

### 🚀 Custom Functions
```powershell
# Quick Navigation Function
function goto($location) {
    Switch ($location) {
        "projects" { Set-Location "D:\Projects" }
        "docs" { Set-Location "C:\Users\$env:USERNAME\Documents" }
        default { Write-Output "Location not found" }
    }
}

# Git Shortcuts
function gs { git status }
function gp { git pull }
function gps { git push }
```

## 🌐 SSH and Remote Connections

### 🔐 SSH Key Generation
```bash
# Generate SSH Key
ssh-keygen -t ed25519 -C "your_email@example.com"
```

### 🖥️ Terminal SSH Profile
```json
{
    "profiles": {
        "list": [
            {
                "name": "Remote Server",
                "commandline": "ssh user@server",
                "icon": "🌐"
            }
        ]
    }
}
```

## 🎛️ Command Palette Magic
- Access with `Ctrl + Shift + P`
- Switch color schemes
- Adjust font size
- Toggle full screen
- Find text
- Open settings

## 🚀 Advanced Launch Options

### 💻 Command Line Arguments
```bash
# Launch specific profile
wt -p "Ubuntu"

# Multiple tabs
wt -p "PowerShell" ; new-tab -p "Ubuntu"
```

### 🎮 Quake Mode
- Toggle: `Win + ~`
- Configure in settings:
```json
{
    "globalSummonHotkeys": "win+~",
    "useQuakeMode": true
}
```

## 🎓 Learning Exercises

### Exercise 1: WSL Exploration
1. Install Ubuntu via Microsoft Store
2. Open Windows Terminal
3. Create a new WSL tab
4. Run `pwd` and explore the filesystem
5. Try running Linux commands like `ls`, `cat`, `grep`

### Exercise 2: PowerShell Customization
1. Create a new function in your PowerShell profile
2. Add a custom alias
3. Reload profile and test your changes

## 📚 Next Learning Paths
- [Troubleshooting Guide](troubleshooting.md)
- [Frequently Asked Questions](faq.md)

## 💡 Pro Tips
- Experiment safely
- Read documentation
- Join terminal communities
- Practice consistently
```