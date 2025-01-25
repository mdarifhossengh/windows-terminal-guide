# Frequently Asked Questions (FAQ) ❓

## 🎯 Learning Objectives
By the end of this guide, you'll:
- Understand Windows Terminal's core features
- Learn advanced configuration techniques
- Discover productivity tips and tricks
- Troubleshoot common issues
- Optimize your terminal workflow

## 🖥️ Windows Terminal Fundamentals

### What is Windows Terminal?
Windows Terminal is a modern, feature-rich terminal application that provides:
- Tabbed command-line interface
- Multi-shell support
- Advanced customization
- Enhanced rendering and performance

### Why Choose Windows Terminal?
🌟 Key Advantages:
- Multiple tabs and panes
- Superior text rendering
- Extensive customization
- Unicode and emoji support
- GPU acceleration
- Cross-shell compatibility

### Supported Shells
- PowerShell
- Command Prompt (CMD)
- Windows Subsystem for Linux (WSL)
- Azure Cloud Shell
- Custom command-line tools

## 🛠️ Configuration Mastery

### Setting Default Profile
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

### Custom Fonts Configuration
```json
{
	"profiles": {
		"defaults": {
			"font": {
				"face": "Cascadia Code",
				"size": 12,
				"weight": "normal"
			}
		}
	}
}
```

### Transparency Effects
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

## 🚀 Advanced Features

### Search Functionality
- `Ctrl + Shift + F`: Open search
- `Enter`: Find next
- `Shift + Enter`: Find previous

### Copy and Paste
- `Ctrl + C`: Copy
- `Ctrl + V`: Paste
- Right-click: Paste
- Text selection auto-copies

### Multi-Command Launching
```bash
# Launch multiple tabs/panes
wt -p "PowerShell" ; new-tab -p "Ubuntu" ; split-pane -p "Command Prompt"
```

## 🎓 Interactive Learning Exercises

### Exercise 1: Profile Customization
1. Open Windows Terminal settings
2. Create a new profile
3. Set a unique color scheme
4. Configure custom font
5. Add a background image

### Exercise 2: Multi-Shell Workflow
1. Open PowerShell tab
2. Create a new Ubuntu WSL tab
3. Split pane with Command Prompt
4. Switch between shells
5. Try cross-shell commands

## 🛠️ Troubleshooting Techniques

### Settings Not Saving?
- Validate JSON syntax
- Check file permissions
- Use VS Code for editing
- Always backup before changes

### Terminal Startup Issues
```bash
# Reset settings
del "%LOCALAPPDATA%\Packages\Microsoft.WindowsTerminal_8wekyb3d8bbwe\LocalState\settings.json"
```

## 💡 Pro Tips and Tricks

### Keyboard Shortcuts
- `Ctrl + Shift + T`: New tab
- `Alt + Arrow`: Switch panes
- `Ctrl + Shift + W`: Close tab/pane
- `Win + ~`: Quake mode

### Command Palette Magic
`Ctrl + Shift + P` enables:
- Color scheme changes
- Font size adjustment
- Pane splitting
- Command discovery

### Custom Actions
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

## 🌟 Best Practices

### Performance Optimization
- Limit startup tasks
- Use GPU acceleration
- Close unused tabs
- Monitor resource usage

### Workflow Organization
- Name tabs descriptively
- Group related panes
- Use color coding
- Create custom profiles

## 📚 Continuous Learning
- [Getting Started](getting-started.md)
- [Customization Guide](customization.md)
- [Advanced Features](advanced-features.md)

## 🌐 Community Resources
- Official Microsoft Docs
- Windows Terminal GitHub
- Stack Overflow
- Reddit r/Windows Terminal
```