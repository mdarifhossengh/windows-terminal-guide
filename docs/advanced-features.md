# Advanced Windows Terminal Features 🚀

Discover powerful features that will enhance your terminal experience.

## Multiple Tabs and Panes

### Tab Management
- `Ctrl + Shift + T` - New tab
- `Ctrl + Shift + D` - Duplicate tab
- `Ctrl + Tab` - Switch tabs
- `Ctrl + Alt + Num` - Switch to specific tab

### Split Panes
```
┌─────────┬─────────┐
│         │         │
│  Pane1  │  Pane2  │
│         │         │
├─────────┴─────────┤
│      Pane3        │
└─────────────────┘
```

- `Alt + Shift + -` - Split horizontally
- `Alt + Shift + +` - Split vertically
- `Alt + Arrow` - Navigate between panes
- `Ctrl + Shift + W` - Close pane

## WSL Integration

### Setting Up WSL
1. Enable WSL:
   ```powershell
   dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
   ```
2. Install Linux distribution from Microsoft Store
3. Configure WSL profile in settings.json:
   ```json
   {
	   "profiles": {
		   "list": [
			   {
				   "guid": "{UUID}",
				   "name": "Ubuntu",
				   "source": "Windows.Terminal.Wsl"
			   }
		   ]
	   }
   }
   ```

### WSL Features
- Automatic path translation
- Integrated file system access
- Seamless clipboard support
- GPU support for WSL 2

## PowerShell Advanced Tips

### Profile Customization
Create/edit PowerShell profile:
```powershell
# Check if profile exists
Test-Path $PROFILE

# Create profile if it doesn't exist
New-Item -Path $PROFILE -Type File -Force

# Edit profile
notepad $PROFILE
```

### Useful PowerShell Functions
```powershell
# Quick directory navigation
function goto($location) {
	Switch ($location) {
		"projects" { Set-Location "D:\Projects" }
		"docs" { Set-Location "C:\Users\$env:USERNAME\Documents" }
		default { Write-Output "Location not found" }
	}
}

# Git shortcuts
function gs { git status }
function gp { git pull }
function gps { git push }
```

## SSH Configuration

### Setting Up SSH
1. Generate SSH key:
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```

2. Configure SSH profile:
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

## Command Palette

Access with `Ctrl + Shift + P`:
- Switch color schemes
- Change font size
- Toggle full screen
- Find text
- Open settings

## Advanced Settings

### Command Line Arguments
Launch with specific profile:
```cmd
wt -p "Ubuntu"
```

Launch multiple tabs:
```cmd
wt -p "PowerShell" ; new-tab -p "Ubuntu"
```

### Quake Mode
- Toggle with `Win + ~`
- Configure in settings:
  ```json
  {
	  "globalSummonHotkeys": "win+~",
	  "useQuakeMode": true
  }
  ```

## Next Steps
- Check [Troubleshooting](troubleshooting.md) for common issues
- Visit [FAQ](faq.md) for more tips