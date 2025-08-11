# Section 6: User Management

This section covers the essentials of managing users and groups in a Linux environment.  
User and group management is a core skill for system administrators, enabling control over system access, security, and collaboration.

## Topics Covered

### 1. Getting User Info
- View current logged-in user: `whoami`
- Display all logged-in users: `who`
- View detailed user information: `id`, `finger`, `getent passwd`

### 2. User Creation
- Create a new user: `sudo adduser <username>`
- Set password for a user: `sudo passwd <username>`

### 3. Changing Users
- Switch to another user: `su <username>`
- Switch to root user: `sudo -i`

### 4. Root Privileges & User Deletion
- Execute commands as root: `sudo <command>`
- Delete a user: `sudo deluser <username>`
- Delete a user along with their home directory:  
  `sudo deluser --remove-home <username>`

### 5. Group Management
- Create a group: `sudo addgroup <groupname>`
- Add a user to a group: `sudo usermod -aG <groupname> <username>`
- Remove a user from a group: `sudo gpasswd -d <username> <groupname>`
- List groups a user belongs to: `groups <username>`

---

## Why This Matters
Proper user and group management helps:
- Maintain system security
- Enforce role-based access control
- Keep multi-user systems organized and efficient
