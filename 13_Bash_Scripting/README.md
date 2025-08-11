# 🐚 Bash Scripting

Bash scripting allows you to automate repetitive tasks, combine multiple commands into reusable programs, and integrate with other tools or languages like Python.

---

## 1. History of Creation, Running Scripts, and Shell

Bash scripts are simply text files containing commands that will be executed by the **Bash shell**.  
To run a script, you usually:
1. Write the script in a text file (e.g., `myscript.sh`).
2. Give it execution permissions.
3. Run it using either `./myscript.sh` or by specifying an interpreter.

---

### Give Execution Rights
```bash
chmod u+x hello_world.sh
````

### Check Interpreter Locations

```bash
whereis bash       # Location of bash interpreter
whereis python3    # Location of python3 interpreter
```

### Identify Current Shell

```bash
echo $0            # Name of current shell
echo $SHELL        # Path to current shell file
cat /etc/shells    # List of all shells installed on this system
```

---

## 2. Example Scripts

### Bash Script — `hello_world.sh`

```bash
#!/bin/bash

echo "Who am I? - " $USER
echo "Where am I? - " $(pwd)
echo "Where? - " $(uname)
echo "Where am I from? - " $HOME
```

**Run the script:**

```bash
./hello_world.sh
```

---

### Python Script — `calendar.py`

```python
#! /usr/bin/python3
# Program to display calendar of the given month and year

import calendar

yy = 2035  # year
mm = 11    # month

# To take month and year input from the user:
# yy = int(input("Enter year: "))
# mm = int(input("Enter month: "))

# display the calendar
print(calendar.month(yy, mm))
```

**Run the script:**

```bash
python3 calendar.py
```

---

## 📌 Section Summary

In this section, you learned:

* How to create and run Bash scripts
* How to check which shell you're using
* How to integrate Bash with other languages like Python

---

### 📜 Commands Learned

```bash
chmod u+x hello_world.sh
whereis bash
whereis python3
echo $0
echo $SHELL
cat /etc/shells
```

---

**💡 Why This Matters:**
Bash scripting is the backbone of automation in Linux.
It allows you to:

* Save time on repetitive tasks
* Create portable tools that work across systems
* Integrate multiple commands into efficient workflows

```
