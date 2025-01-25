# Troubleshooting Windows Terminal 🔧

Common issues and their solutions to help you resolve Windows Terminal problems.

## Common Issues

### Terminal Won't Launch

1. **Missing Dependencies**
   - Ensure Windows 10 version 1903 or later
   - Check Microsoft Store for updates
   - Reinstall Windows Terminal

2. **Corrupted Settings**
   ```powershell
   # Backup settings
   Copy-Item "$env:LOCALAPPDATA\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json" "$env:USERPROFILE\Desktop\terminal_backup.json"
   
   # Delete settings to reset
   Remove-Item "$env:LOCALAPPDATA\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json"
   ```

### Performance Issues

1. **Slow Startup**
   - Disable startup scripts in profile
   - Check antivirus exclusions
   - Reduce acrylic transparency

2. **High CPU Usage**
   - Disable GPU acceleration
   - Update graphics drivers
   - Reduce number of active panes

### Visual Glitches

1. **Font Issues**
   - Verify font installation
   - Try default Cascadia Code
   - Clear font cache:
   ```cmd
   fc-cache -f -v
   ```

2. **Display Problems**
   - Update Windows
   - Update graphics drivers
   - Disable acrylic effects

### WSL Problems

1. **WSL Not Working**
   ```powershell
   # Check WSL status
   wsl --status
   
   # Update WSL
   wsl --update
   
   # Restart WSL
   wsl --shutdown
   ```

2. **Path Issues**
   - Check path conversion
   - Verify WSL installation
   - Update WSL version

## Error Messages

### Common Error Codes

1. **0x80070002**
   - File not found
   - Check file paths
   - Verify permissions

2. **0x80004005**
   - Access denied
   - Run as administrator
   - Check folder permissions

### Profile Errors

1. **Invalid Profile Settings**
   - Validate JSON syntax
   - Check GUID format
   - Verify file paths

2. **Missing Profile**
   ```json
   {
	   "profiles": {
		   "defaults": {},
		   "list": [
			   {
				   "guid": "{...}",
				   "name": "PowerShell",
				   "commandline": "powershell.exe"
			   }
		   ]
	   }
   }
   ```

## Performance Tips

1. **Optimize Settings**
   - Disable unused features
   - Reduce history size
   - Limit startup tasks

2. **Memory Management**
   - Close unused tabs
   - Limit concurrent processes
   - Monitor resource usage

## Recovery Steps

1. **Backup Important Data**
   ```powershell
   # Backup all settings
   $backupPath = "$env:USERPROFILE\Desktop\terminal_backup"
   New-Item -ItemType Directory -Force -Path $backupPath
   Copy-Item "$env:LOCALAPPDATA\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\*" $backupPath
   ```

2. **Clean Installation**
   - Uninstall Windows Terminal
   - Remove settings folder
   - Reinstall from Store

## Next Steps
- Review [FAQ](faq.md) for more solutions
- Check [Customization](customization.md) for optimal settings