# Nmap Scanning Lab – Ethical Hacking Recon Walkthrough

This repository demonstrates several Nmap scanning techniques for ethical hacking and penetration testing. The scans were performed in a **controlled lab environment** against a setup virtual LAN.

## Tools Used

- 🛠️ Nmap (Network Mapper)
- 📸 Screenshots of each scan result


## Scanning Techniques Demonstrated

Scan Type               | Command Used                                                                 

Aggressive Scan        | `nmap -A 192.168.1.106`                                                       
Host Discovery         | `nmap -sn 192.168.1.0/24`                                                     
Script + Version Scan  | `nmap -sC -sV 192.168.1.106`                                                  
OS Detection           | `nmap -O 192.168.1.106`                                                       
Version Detection Only | `nmap -sV 192.168.1.106`                                                      
SMTP User Enumeration  | `nmap --script=smtp-enum-users -p 25 192.168.1.106`                           

---

## Screenshots Included

- `Aggressive scanning.png`
- `Host Discovery.png`
- `Nmap enumeration script.png`
- `Service version.png`
- `Operating system.png`
- `Port scanning.png`
- `Host Discovery.png`


## ⚠️ Disclaimer

This project is for educational purposes only. **Do not scan unauthorized systems.** All scans were performed in a lab using virtual machines I own.

---

## 📘 Walkthrough

See [`WALKTHROUGH.md`](./WALKTHROUGH.md) for a full step-by-step explanation of each scan.
