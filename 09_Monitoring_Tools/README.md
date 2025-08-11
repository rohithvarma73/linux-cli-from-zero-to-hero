# 📊 Section 9 — Monitoring Tools

Monitoring tools are essential for **understanding system performance**, **managing processes**, and **ensuring services run smoothly**.  
They help troubleshoot issues, maintain stability, and optimize resources.

---

## 1. Top Utility (Task Manager)

`top` is a real-time, interactive utility that displays:
- CPU and memory usage
- Running processes
- Load averages
- Process IDs (PIDs)

**Common Usage**
```bash
top                  # Start top
top -o PID           # Sort processes by PID
top -u salesguy      # Show processes for user 'salesguy'
````

**Interactive Keys**

| Key | Description             |
| --- | ----------------------- |
| `q` | Quit top                |
| `k` | Kill process            |
| `M` | Sort by memory usage    |
| `P` | Sort by CPU usage       |
| `1` | Show per-core CPU usage |
| `h` | Help menu               |

**Why Use It?**

* Quickly spot resource-heavy processes
* Monitor system load in real time
* Debug performance bottlenecks

---

## 2. htop, ps, kill, systemctl Utilities

### htop

A more user-friendly, interactive process viewer.

**Install & Run**

```bash
sudo apt-get install htop
htop
```

**Features**

* Navigate with arrow keys
* Kill processes with `F9`
* Sort easily with function keys
* Search with `/`

---

### ps (Process Status)

Displays snapshots of current processes.

**Usage**

```bash
ps             # Show processes for the current shell
ps 1           # Info about process ID 1
ps aux         # All processes in table format
ps afx         # Processes in tree format
```

---

### pidof

Finds the PID of a process by name.

```bash
pidof process_name
```

---

### kill

Terminates processes by PID.

```bash
kill PID          # Graceful termination
kill -15 PID      # Default signal (TERM)
kill -9 PID       # Force kill (KILL)
```

---

### systemctl (Service Manager)

Controls and inspects services.

**Usage**

```bash
systemctl              # Manage systemd services
systemctl status ssh   # Show SSH service status
systemctl stop ssh     # Stop SSH service
systemctl start ssh    # Start SSH service
systemctl is-active ssh # Check if SSH is running
```

---

## 📌 Section Summary

Monitoring tools are your **first line of defense** against performance issues.
They let you:

* Identify heavy resource usage
* Kill unresponsive processes
* Manage background services
* Keep your system stable and efficient

---

### 📜 Commands Learned

```bash
top -o PID                # Run top sorted by PID
top -u salesguy           # Filter top by user

sudo apt-get install htop # Install htop
ps                        # Show current process info
ps 1                      # Info for process #1
ps aux                    # Table of all processes
ps afx                    # Process tree

pidof process_name        # Find PID by name

kill PID                  # Kill process
kill -15 PID              # Graceful terminate
kill -9 PID               # Force kill

systemctl status ssh      # Show SSH service status
systemctl stop ssh        # Stop SSH
systemctl start ssh       # Start SSH
systemctl is-active ssh   # Check SSH status
```

---

**💡 Why This Matters:**
Whether you're debugging a slow machine, managing server resources, or keeping critical services running, **mastering monitoring tools is a core skill for every Linux administrator**.
