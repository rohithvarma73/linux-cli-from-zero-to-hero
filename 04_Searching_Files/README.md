# Searching Files

## Overview
This section covers essential techniques for locating files and directories in a Linux system. You will explore folder structures and learn to use the versatile `find` command for targeted searches.

---

## Topics Covered
1. **Folder Structure** — Understanding how Linux organizes files and directories.  
2. **Find Command** — Searching for files and directories based on name, type, size, modification time, and more.

---

## Section Summary
By the end of this section, you will be able to:
- Navigate and interpret the Linux directory structure
- Use `find` to search for files and folders efficiently
- Combine `find` with other commands for advanced search operations

---

## List of Learned Commands

### Folder Structure
- `/` — Root directory of the filesystem  
- `/home` — User home directories  
- `/etc` — Configuration files  
- `/var` — Variable data files  
- `/usr` — User programs and data  
- `/tmp` — Temporary files  

### Find Command
- `find <path>` — Search from a specific directory  
- `find <path> -name "<filename>"` — Search by exact name  
- `find <path> -iname "<filename>"` — Case-insensitive search  
- `find <path> -type f` — Search for files only  
- `find <path> -type d` — Search for directories only  
- `find <path> -size +1M` — Search for files larger than 1MB  
- `find <path> -mtime -7` — Search for files modified in the last 7 days  
- `find <path> -exec <command> {} \;` — Execute a command on search results

---
"@ | Set-Content -Path "04_Searching_Files/README.md"
