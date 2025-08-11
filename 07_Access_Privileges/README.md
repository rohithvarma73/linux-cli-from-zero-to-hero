# Access Privileges

This section explains how to view and manage file and directory permissions in Linux.  
Proper permission management ensures that only authorized users can read, modify, or execute files, helping maintain system security.

## Topics Covered

### 1. Getting Info + `chmod` Command
- View file permissions:  
  `ls -l` → Output format: `-rwxr-xr--`
- Permission categories:  
  - **Owner** → The user who owns the file  
  - **Group** → Users in the file's group  
  - **Others** → All other users
- Change permissions with `chmod`:
  - Symbolic mode: `chmod u+x file.txt` (add execute permission for user)
  - Numeric mode: `chmod 755 file.txt` (rwxr-xr-x)

### 2. Changing File Owners
- Change file owner:  
  `sudo chown newuser file.txt`
- Change group ownership:  
  `sudo chgrp newgroup file.txt`
- Change both owner and group:  
  `sudo chown newuser:newgroup file.txt`

### 3. Special Bits & Default Permissions
- **Setuid (s)** → Execute file with the permissions of the file owner
- **Setgid (s)** → New files in a directory inherit the group ID
- **Sticky bit (t)** → Only file owner can delete files in a directory
- View special bits: `ls -l` (look for `s` or `t`)
- Set special bits:
  - Setuid: `chmod u+s file`
  - Setgid: `chmod g+s directory`
  - Sticky bit: `chmod +t directory`
- Default permissions:
  - Controlled by `umask`
  - View current `umask` value: `umask`
  - Change default permissions: `umask 022`

---

## Why This Matters
- Prevents unauthorized data access or modification
- Allows collaborative work without compromising security
- Helps enforce best practices in file management
