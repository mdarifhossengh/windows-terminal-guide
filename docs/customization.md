# Customizing Windows Terminal 🎨

Learn how to personalize your Windows Terminal experience with themes, colors, fonts, and more.

## Settings Overview

To access settings:
1. Click `⌄` in the tab bar
2. Select "Settings"
   - Or use `Ctrl + ,` shortcut
3. Settings open in your default JSON editor

## Color Schemes

### Built-in Schemes
Windows Terminal comes with several pre-installed color schemes:
- Campbell (Default)
- One Half Dark
- One Half Light
- Solarized Dark
- Solarized Light

### Custom Color Scheme
Add your own scheme in settings.json:
```json
{
	"schemes": [
		{
			"name": "My Custom Theme",
			"background": "#0C0C0C",
			"foreground": "#CCCCCC",
			"black": "#0C0C0C",
			"blue": "#0037DA",
			"cyan": "#3A96DD",
			"green": "#13A10E",
			"purple": "#881798",
			"red": "#C50F1F",
			"white": "#CCCCCC",
			"yellow": "#C19C00"
		}
	]
}
```

## Font Configuration

### Changing Fonts
1. Open Settings
2. Select your profile
3. Under "Appearance":
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

### Recommended Fonts
- Cascadia Code (Default)
- Fira Code
- JetBrains Mono
- Source Code Pro

## Profile Settings

### Basic Profile Configuration
```json
{
	"profiles": {
		"defaults": {
			"colorScheme": "One Half Dark",
			"cursorShape": "bar",
			"fontFace": "Cascadia Code",
			"fontSize": 12,
			"opacity": 95,
			"padding": "8",
			"snapOnInput": true,
			"useAcrylic": true
		}
	}
}
```

### Background Effects
1. Acrylic (Transparency):
   ```json
   {
	   "useAcrylic": true,
	   "acrylicOpacity": 0.8
   }
   ```

2. Background Image:
   ```json
   {
	   "backgroundImage": "C:\\path\\to\\image.png",
	   "backgroundImageOpacity": 0.3,
	   "backgroundImageStretchMode": "fill"
   }
   ```

## Keyboard Shortcuts

### Custom Key Bindings
Add to settings.json:
```json
{
	"keybindings": [
		{
			"command": "newTab",
			"keys": "ctrl+t"
		},
		{
			"command": "closeTab",
			"keys": "ctrl+w"
		}
	]
}
```

## Tips for Customization

1. Backup your settings before making changes
2. Use the settings UI for basic changes
3. Edit settings.json directly for advanced customization
4. Test changes incrementally
5. Use comments in JSON for documentation

## Next Steps
- Explore [Advanced Features](advanced-features.md)
- Check [Troubleshooting](troubleshooting.md) if issues arise