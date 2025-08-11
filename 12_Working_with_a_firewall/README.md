# 🔥 Working with Firewall

A firewall in Linux is a security system that filters incoming and outgoing network traffic based on rules you define.  
**iptables** is one of the most common firewall management tools in Linux, allowing you to view, add, delete, and save rules.

---

## 1. View, Add, Delete Rules

**View Current Rules**
```bash
sudo iptables -L                      # Display current rules
sudo iptables -L -nv --line-numbers   # Display detailed rules with line numbers
````

**Add Logging Rules**

```bash
sudo iptables -A INPUT -j LOG         # Log all incoming requests
sudo iptables -A OUTPUT -j LOG        # Log all outgoing requests
sudo iptables -A FORWARD -j LOG       # Log all transit (forwarded) requests
```

**Block or Allow Specific IPs**

```bash
sudo iptables -t filter -A INPUT -s 192.168.0.104 -j DROP   # Block IP
sudo iptables -t filter -A INPUT -s 192.168.0.107 -j ACCEPT # Allow IP
```

**Delete a Rule**

```bash
sudo iptables -t filter -D INPUT 4    # Delete rule #4 in the INPUT chain
```

**Block Specific Ports**

```bash
sudo iptables -A OUTPUT -p tcp --dport 80 -j REJECT # Block HTTP requests
```

---

## 2. Default Policies & Save Rules

**Set Default Policy**

```bash
sudo iptables -P INPUT DROP           # Drop all incoming requests by default
sudo iptables -P INPUT ACCEPT         # Allow all incoming requests by default
```

**Allow Specific Ports**

```bash
sudo iptables -I INPUT -p tcp --dport 22 -j ACCEPT # Allow SSH requests
```

**Save & Restore Rules**

```bash
sudo iptables-save > ~/iptables_config    # Save rules to a file
sudo iptables-restore < ~/iptables_config # Restore rules from a file
```

---

## 3. Useful Networking Commands

```bash
hostname -I    # Show IP address
ip a           # Show network interfaces and IPs
```

---

## 📌 Section Summary

The **iptables** utility gives you fine-grained control over network access, allowing you to:

* View and manage firewall rules
* Block or allow specific IPs or ports
* Set default policies for security
* Save and restore configurations

---

### 📜 Commands Learned

```bash
sudo apt install iptables
sudo iptables -L
sudo iptables -A INPUT -j LOG
sudo iptables -F INPUT
sudo iptables -A OUTPUT -j LOG
sudo iptables -A FORWARD -j LOG
hostname -I
ip a
sudo iptables -t filter -A INPUT -s <IP> -j DROP
sudo iptables -t filter -A INPUT -s <IP> -j ACCEPT
sudo iptables -L -nv --line-numbers
sudo iptables -t filter -D INPUT <rule_number>
sudo iptables -A OUTPUT -p tcp --dport 80 -j REJECT
sudo iptables -P INPUT DROP
sudo iptables -P INPUT ACCEPT
sudo iptables -I INPUT -p tcp --dport 22 -j ACCEPT
sudo iptables-save > ~/iptables_config
sudo iptables-restore < ~/iptables_config
```

---

**💡 Why This Matters:**
A properly configured firewall is one of the first lines of defense against malicious access.
With **iptables**, you can allow only the traffic you trust, block harmful connections, and ensure network security both inbound and outbound.

```
