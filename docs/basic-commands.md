# Basic Terminal Commands 🔧

## 🎯 Learning Objectives
By the end of this guide, you'll:
- Master essential terminal navigation
- Perform file and directory operations
- Understand system commands
- Develop confidence in terminal usage

## 🧭 Navigation Mastery

### 📂 Directory Navigation
```bash
# Show current directory
pwd  # PowerShell
dir  # Command Prompt

# Change directories
cd Documents           # Move to Documents
cd ..                  # Move up one level
cd \                   # Go to root
cd C:\Users\YourName   # Absolute path
```

#### 💡 Pro Tips
- Use `Tab` for auto-completion
- `Shift + Right/Left Arrow` selects text
- `Ctrl + L` clears screen

### 🔍 Listing and Exploring
```bash
# List directory contents
dir             # Basic listing
dir /a          # Show hidden files
dir /w          # Wide format
ls              # PowerShell alias
```

## 📁 File and Directory Operations

### 📋 File Management
```bash
# Copy files
copy source.txt destination.txt
copy *.txt backup\     # Copy multiple files

# Move/Rename files
move old.txt new.txt
move document.txt Documents\

# Delete files
del file.txt
del *.tmp       # Delete temp files
```

### 📂 Directory Management
```bash
# Create directories
mkdir NewFolder
mkdir "Folder with Spaces"

# Remove directories
rmdir EmptyFolder
rmdir /s /q NonEmptyFolder  # Force remove
```

## 🖥️ System Insights

### 🔧 System Information Commands
```bash
# System details
systeminfo      # Comprehensive system info
ver             # Windows version
ipconfig        # Network configuration
```

### 🚦 Process Management
```bash
# List running processes
tasklist

# End processes
taskkill /IM notepad.exe    # By name
taskkill /PID 1234          # By Process ID
```

## 🎓 Learning Exercises

### Exercise 1: Navigation Challenge
1. Open terminal
2. Navigate to your Documents folder
3. Create a new folder called "TerminalPractice"
4. Create three text files inside: notes1.txt, notes2.txt, notes3.txt
5. Copy all files to a backup subfolder

### Exercise 2: System Exploration
1. Run `systeminfo` and identify:
   - Windows version
   - Processor type
   - Total physical memory

## 🚨 Common Pitfalls
- Always use quotes for paths with spaces
- Be careful with `del` and `rmdir /s /q`
- Use `Tab` for accurate file/folder names

## 🔄 CMD vs PowerShell Cheat Sheet
| Operation | CMD       | PowerShell |
|-----------|-----------|------------|
| List      | `dir`     | `ls`       |
| Copy      | `copy`    | `cp`       |
| Move      | `move`    | `mv`       |
| Delete    | `del`     | `rm`       |

## 📚 Next Learning Paths
- [Advanced Terminal Features](advanced-features.md)
- [Terminal Customization](customization.md)

## 💡 Final Tips
- Practice daily
- Experiment safely
- Use `command /?` for help
```