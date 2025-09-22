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


1. **Identify the Local IP and Subnet**
   - First, I ran the following command to find my machine’s IP address and subnet:
   ```bash
   ip addr show
Output showed my IP: 172.20.10.2/28, which means my subnet is 172.20.10.0/28.

2. **Perform TCP SYN Scan**
   - To detect live hosts and open ports in the subnet, I ran:
   ```bash
   sudo nmap -sS 172.20.10.0/28
This scan helped identify which IPs were active and which ports were open.


This scan detected which IPs were active and which ports were open.

3. **Service & Version Detection**
   - To identify the services running on open ports, I ran:
   ```bash
   sudo nmap -sV 172.20.10.0/28
Nmap returned the service names and versions where possible.

4. **Vulnerability Scan Using Nmap Scripts**
   - To check for known vulnerabilities, I combined SYN scan, version detection, and Nmap scripts:
   ```bash
   sudo nmap -sS -sV --script vuln 172.20.10.0/28 -oN scan_results.txt
Results were saved to scan_results.txt for documentation.
