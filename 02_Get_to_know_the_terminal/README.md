@"
# Get to Know the Terminal

## Overview
This section covers essential Linux terminal tips, hotkeys, and basic commands for navigating, creating, and managing files and folders. You'll also learn various ways to view and manipulate file content.

---

## Topics Covered
- Terminal tips and tricks
- List of Linux terminal hotkeys
- Basic navigation commands
- Creating files and folders
- Basic file operations
- Viewing files

---

## Section Summary
This section provided hands-on experience with:
- Navigating the Linux file system
- Managing files and directories
- Using built-in help systems
- Viewing and editing file content directly from the terminal

---

## List of Learned Commands

### Terminal Utilities
- `clear` — Clear the terminal window
- `reset` — Reset terminal settings
- `whatis` — One-line help for commands
- `<command> --help` — Brief help on commands
- `man`, `info` — Detailed help on commands
- `apropos` — Search by reference
- `history` — Output command history

### Navigation
- `pwd` — Print the current working directory
- `cd` — Change the current directory
- `ls` — List directory contents
- `ll` — Alias for `ls -la`

### File & Directory Management
- `mkdir` — Create a new folder
- `tree` — Display the file structure as a tree
- `touch` — Create an empty file
- `echo` — Display text or write it to a file
- `cat` — Concatenate and display file contents

### Copy, Move, and Delete
- `cp` — Copy a file or folder
- `mv` — Move or rename a file or folder
- `rm` — Delete a file or folder

### Viewing File Contents
- `more` — View file contents one page at a time
- `less` — Similar to `more` but with more navigation features
- `head` — View the first lines of a file
- `tail` — View the last lines of a file

---
"@ | Set-Content -Path "02_Get_to_know_the_terminal/README.md"
