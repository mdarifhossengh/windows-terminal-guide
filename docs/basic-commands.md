# Basic Terminal Commands 🔧

This guide covers essential commands you'll use frequently in Windows Terminal.

## Navigation Commands

### Directory Navigation
- `dir` - List contents of current directory
	```cmd
	dir
	dir /a    # Show hidden files
	dir /w    # Wide list format
	```

- `cd` - Change directory
	```cmd
	cd Documents           # Move to Documents folder
	cd ..                 # Move up one level
	cd \                  # Move to drive root
	cd C:\Users\Username  # Move to specific path
	```

- `pwd` (PowerShell) - Show current directory
	```powershell
	pwd
	# or
	Get-Location
	```

## File Operations

### File Management
- `copy` - Copy files
	```cmd
	copy source.txt destination.txt
	copy *.txt backup\    # Copy all .txt files
	```

- `move` - Move/rename files
	```cmd
	move old.txt new.txt          # Rename file
	move document.txt Documents\   # Move file
	```

- `del` - Delete files
	```cmd
	del file.txt
	del *.tmp           # Delete all .tmp files
	```

### Directory Operations
- `mkdir` or `md` - Create directory
	```cmd
	mkdir NewFolder
	mkdir "New Folder"   # With spaces
	```

- `rmdir` or `rd` - Remove directory
	```cmd
	rmdir EmptyFolder
	rmdir /s /q Folder  # Remove non-empty folder
	```

## System Commands

### System Information
- `systeminfo` - Display system information
- `tasklist` - Show running processes
- `ipconfig` - Show network configuration

### Process Management
- `taskkill` - End a process
	```cmd
	taskkill /IM notepad.exe    # Kill by name
	taskkill /PID 1234          # Kill by process ID
	```

## Tips & Tricks

1. Use `Tab` for auto-completion
2. Press `↑` to cycle through command history
3. Use `cls` to clear the screen
4. Add `/help` or `/?` to any command for help:
	 ```cmd
	 dir /?
	 ```

## PowerShell Equivalents

Many CMD commands have PowerShell aliases:
- `ls` = `dir`
- `rm` = `del`
- `cp` = `copy`
- `mv` = `move`

## Next Steps
- Learn about [Customization](customization.md)
- Explore [Advanced Features](advanced-features.md)