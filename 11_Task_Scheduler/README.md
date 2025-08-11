# ⏳ Task Scheduler

The Linux task scheduler allows you to automate repetitive tasks, such as running backups, cleaning temporary files, sending reports, or executing scripts at fixed intervals.  
In most Linux distributions, this is done using the **cron service** and the **crontab** utility.

---

## 1. Cron Service

The **cron service** is a background process (daemon) that executes scheduled tasks at specific times and dates.  
It reads configuration files called **crontabs** which contain the timing rules and commands.

**Basic Management Commands**
```bash
systemctl status cron      # Check the status of the cron service
sudo systemctl start cron  # Start the cron service
````

---

## 2. Crontab Utility

The **crontab** utility is used to create, view, edit, and delete scheduled tasks for specific users.

**Basic Usage**

```bash
crontab -l                 # List scheduled commands for the current user
crontab -e                 # Edit the current user's scheduled tasks
crontab -r                 # Remove the current user's scheduled tasks
```

**Working with Other Users**

```bash
crontab -u user_name -e    # Edit another user's scheduled tasks (requires sudo)
```

---

## 3. Setting Up Logs

Cron automatically logs task execution in:

```bash
/var/log/syslog       # On Debian/Ubuntu
/var/log/cron         # On RHEL/CentOS
```

To monitor cron activity in real-time:

```bash
tail -f /var/log/syslog | grep CRON
```

---

## 📌 Section Summary

The **cron service** and **crontab** utility are essential for automation in Linux.
They:

* Run scripts and commands automatically on a defined schedule
* Allow per-user scheduling
* Support logging for monitoring and debugging
* Can be managed centrally by the system administrator

---

### 📜 Commands Learned

```bash
systemctl status cron
sudo systemctl start cron
crontab -l
crontab -e
crontab -r
crontab -u user_name -e
```

---

**💡 Why This Matters:**
Automating tasks saves time, reduces human error, and ensures important processes (like backups, cleanup scripts, or data collection) happen reliably — even when you’re away from the terminal.

---
