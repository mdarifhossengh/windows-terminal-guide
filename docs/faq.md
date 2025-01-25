# Frequently Asked Questions (FAQ) ❓

Common questions and answers about Windows Terminal.

## General Questions

### What is Windows Terminal?
Windows Terminal is a modern terminal application that provides a tabbed command-line interface for Windows, supporting multiple shells like PowerShell, Command Prompt, and WSL.

### Why use Windows Terminal over Command Prompt?
- Multiple tabs and panes
- Better text rendering
- Custom themes and fonts
- Rich customization options
- Modern features like copy/paste
- Unicode and emoji support
- GPU acceleration

### Which shells can I use?
- PowerShell
- Command Prompt (CMD)
- Windows Subsystem for Linux (WSL)
- Azure Cloud Shell
- Any custom shell or command-line tool

## Configuration

### How do I set a default profile?
```json
{
	"defaultProfile": "{GUID}",
	"profiles": {
		"list": [
			{
				"guid": "{GUID}",
				"name": "PowerShell"
			}
		]
	}
}
```

### Can I use custom fonts?
Yes! Install a monospace font and add to settings:
```json
{
	"profiles": {
		"defaults": {
			"font": {
				"face": "Your Font Name"
			}
		}
	}
}
```

### How do I enable transparency?
```json
{
	"profiles": {
		"defaults": {
			"useAcrylic": true,
			"acrylicOpacity": 0.7
		}
	}
}
```

## Features

### Can I search in Terminal?
Yes! Use:
- `Ctrl + Shift + F` - Open search
- `Enter` - Find next
- `Shift + Enter` - Find previous

### How do I copy/paste?
- `Ctrl + C` - Copy
- `Ctrl + V` - Paste
- Right-click - Paste
- Select text automatically copies

### Can I run multiple commands?
Yes, using semicolons:
```cmd
wt -p "PowerShell" ; new-tab -p "Ubuntu" ; split-pane -p "Command Prompt"
```

## Troubleshooting

### Why won't my settings save?
- Check JSON syntax
- Verify file permissions
- Use VS Code for editing
- Backup before changes

### Terminal crashes on startup?
1. Reset settings:
   ```cmd
   del "%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json"
   ```
2. Restart Terminal

### Missing features?
- Update Windows Terminal
- Check Windows version
- Verify installation

## Tips and Tricks

### Keyboard Shortcuts
- `Ctrl + Shift + T` - New tab
- `Alt + Arrow` - Switch panes
- `Ctrl + Shift + W` - Close tab/pane
- `Win + ~` - Quake mode

### Command Palette
Access with `Ctrl + Shift + P`:
- Change color scheme
- Adjust font size
- Split panes
- Find commands

### Custom Actions
Add custom commands:
```json
{
	"actions": [
		{
			"command": "openNewTabDropdown",
			"keys": "ctrl+alt+t"
		}
	]
}
```

## Best Practices

1. **Regular Backups**
   - Backup settings.json
   - Save custom profiles
   - Document changes

2. **Performance**
   - Limit startup tasks
   - Use GPU acceleration
   - Close unused tabs

3. **Organization**
   - Name tabs clearly
   - Group related panes
   - Use color coding

## See Also
- [Getting Started](getting-started.md)
- [Customization](customization.md)
- [Advanced Features](advanced-features.md)