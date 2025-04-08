# 🧭 Nmap Scanning Walkthrough

This walkthrough explains each Nmap scan in detail with explanations and examples from my LAN setup.

---

## 1. Aggressive Scan

**Command:**

nmap -A 10.10.10.0/24

Includes:

OS detection

Version detection

Script scan

Traceroute

📸 Screenshot: Aggressive scanning.png

🧠 Learnings:

OS fingerprint

Service versions

Possible CVEs from service banners

2. Host Discovery (Ping Sweep)
Command:

nmap -sn 10.10.10.0/24
📸 Screenshot: Host Discovery.png

🧠 Learnings:

List of live IPs in the subnet

No ports scanned — only host status

3. Default Script + Version Detection
Command:

nmap -sC -sV 10.10.10.0/24
📸 Screenshot: Nmap enumeration script.png

🧠 Learnings:

Service versions

Script outputs (like anonymous FTP login, outdated HTTP servers)

Potential SMB shares or usernames

🔍 4. OS Detection
Command:

nmap -O 10.10.10.0/24
🧠 Learnings:

Tries to guess the target's operating system based on TCP/IP stack fingerprinting

Useful in determining Linux/Windows and OS version

🎯 5. Version Detection
Command:

nmap -sV 10.10.10.0/24
🧠 Learnings:

Helps identify vulnerable versions of services

Example: Apache 2.2.8 might be vulnerable to known CVEs

📬 6. SMTP User Enumeration
Command:

nmap --script=smtp-enum-users -p 25 10.10.10.19
🧠 Learnings:

Enumerates possible email users via SMTP VRFY or EXPN

Great for brute-force attack surface mapping in social engineering or phishing scenarios

Summary of Flags Used
Flag	Description
-A	Aggressive scan (OS, versions, scripts, traceroute)
-sn	Host discovery (ping sweep)
-sC	Run default scripts
-sV	Service version detection
-O	OS fingerprinting
--script=smtp-enum-users	SMTP user enumeration

Best Practices
Always scan with permission.

Start with stealthy scans, escalate only if needed.

Review each scan result to guide your next recon step.

Legal Use Only
This walkthrough is for educational and ethical use. Unauthorized scanning may violate laws and network policies.