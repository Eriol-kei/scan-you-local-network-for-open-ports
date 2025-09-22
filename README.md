# scan-you-local-network-for-open-ports
learn to discover open ports on devices in your local network to understand network experience

This repository contains the results of network scanning experiments performed using [Nmap](https://nmap.org/) on a controlled lab network.

---

## 📌 Overview

- **Subnet scanned:** 172.20.10.0/28 (16 IPs)
- **Hosts detected:** 3
- **Purpose:** Educational and research purposes only
- **Tools used:** Nmap, optionally Wireshark

---

## 💻 Commands Used

All scans were performed in a **controlled environment**. The exact command to generate these results:

```bash
sudo nmap -sS -sV --script vuln 172.20.10.0/28 -oN scan_results.txt
