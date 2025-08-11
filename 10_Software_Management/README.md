# 💻 Software Management

Software management in Linux involves installing, updating, and removing packages, as well as managing repositories and package sources.  
Mastering these tools ensures your system is **up-to-date**, **secure**, and **running only what you need**.

---

## 1. apt / apt-get Utility

**apt** and **apt-get** are command-line tools for managing Debian-based systems (Ubuntu, etc.).

**Basic Commands**
```bash
sudo apt update         # Update list of packages from repositories
sudo apt upgrade -y     # Upgrade all installed packages
sudo apt-get install htop  # Install htop utility
sudo apt-get remove htop   # Remove htop
sudo apt-get purge htop    # Remove htop + its config files
````

**Fun Extras**

```bash
apt moo                 # Easter egg
aptitude moo -vvvvv     # Another Easter egg
sudo apt install cowsay # Talking cow program
```

---

## 2. dpkg and snap Utilities

### dpkg

A low-level package manager for `.deb` packages.

**Examples**

```bash
dpkg -l                 # List all installed packages
dpkg -l | wc -l         # Count installed packages
dpkg -l tree            # Info about the tree package
apt show tree           # Show package info (using apt)
apt download htop       # Download .deb file without installing
sudo dpkg -i htop_3.0-11_amd64.deb  # Install a .deb file
```

### snap

A modern, universal package manager.

**Examples**

```bash
sudo apt install snapd     # Install snap
snap find opera            # Search snap packages
snap list                  # List installed snap packages
sudo snap install opera    # Install Opera browser
sudo snap remove opera     # Remove Opera browser
```

---

## 3. Adding a Repository

Repositories provide software sources for installation. Adding new ones allows you to install packages not available in default repos.

**Example: Adding VirtualBox Repository**

```bash
# Download VirtualBox deb package
wget https://download.virtualbox.org/virtualbox/7.1.4/virtualbox-7.1_7.1.4-165100~Ubuntu~jammy_amd64.deb

# Install deb package
sudo dpkg -i virtualbox-7.1_7.1.4-165100~Ubuntu~jammy_amd64.deb

# Remove package
sudo dpkg -r virtualbox-7.1
```

**Working with apt Sources**

```bash
ls /etc/apt
cd /etc/apt
ll
cat sources.list

# Create new repo file
sudo nano sources.list.d/vbox.list

# View repo directory
ls sources.list.d
tree
cat sources.list.d/vbox.list
```

**Add VirtualBox Repo Key**

```bash
wget -O- https://www.virtualbox.org/download/oracle_vbox_2016.asc \
| sudo gpg --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg --dearmor
```

**Refresh and Install**

```bash
sudo apt update
sudo apt install virtualbox
```

**Confirm Installation**

```bash
whatis virtualbox
virtualbox --help
```

---

## 4. Useful Extras

**Get Distribution Info**

```bash
lsb_release -a
```

**Working with add-apt-repository**

```bash
man add-apt-repository
sudo apt install software-properties-common
```

---

## 📌 Section Summary

Software management tools let you:

* Install, remove, and update software packages
* Work with `.deb` files and universal snap packages
* Add repositories for extra software sources
* Keep your system stable and functional

---

### 📜 Commands Learned

```bash
sudo apt update
sudo apt upgrade -y
sudo apt-get install htop
sudo apt-get remove htop
sudo apt-get purge htop
apt moo
aptitude moo -vvvvv
sudo apt install cowsay

dpkg -l
dpkg -l | wc -l
dpkg -l tree
apt show tree
apt download htop
sudo dpkg -i htop_3.0-11_amd64.deb
sudo apt install snapd
apt search opera
snap find opera
snap list
sudo snap install opera
sudo snap remove opera

wget https://download.virtualbox.org/.../virtualbox-7.1_7.1.4-165100~Ubuntu~jammy_amd64.deb
sudo dpkg -i virtualbox-7.1_7.1.4-165100~Ubuntu~jammy_amd64.deb
sudo dpkg -r virtualbox-7.1

ls /etc/apt
cd /etc/apt
ll
cat sources.list
sudo nano sources.list.d/vbox.list
ls sources.list.d
tree
cat sources.list.d/vbox.list

wget -O- https://www.virtualbox.org/download/oracle_vbox_2016.asc \
| sudo gpg --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg --dearmor

sudo apt update
sudo apt install virtualbox

whatis virtualbox
virtualbox --help

lsb_release -a
man add-apt-repository
sudo apt install software-properties-common
```

---

**💡 Why This Matters:**
Efficient software management is a cornerstone of Linux administration.
It ensures your system has the **right tools**, **updated packages**, and **secure repositories** without clutter or outdated software.

