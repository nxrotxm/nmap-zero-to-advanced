# 🔍 Nmap Complete Guide (Beginner to Advanced)

## 📘 Introduction

Nmap (Network Mapper) is a powerful tool used for network discovery and security auditing.

These are used in initial reconnaissance (beginner level)

---

## ⚙️ Lab Setup

* Kali Linux (Attacker)
* Metasploitable2 (Target)

---

## 🧠 Chapter 1: Basic Commands for Scanning

### 🔹 Command 1 : Host Discovery scan

 ![Nmap](https://img.shields.io/badge/nmap%20--sn%20192.168.198.0/24-red)

### 📌 Description:

- scan entire network and display available hosts.

### 📷 Output:

![Basic Scan](screenshots/host-discovery-scan.png)

---

### 🔹 Command 2 : Basic scan/default scan

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.129-red)

### 📌 Description:

- Default scan of nmap.
- Used to quickly identify open ports.
- Scan top 1000 common ports and displays all open ports with running service with that port.

### 📷 Output:

![Basic Scan](screenshots/basic-scan.png)

---

### 🔹 Command 3 : Multiple Target scan

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.129%20192.168.198.2-red)

### 📌 Description:

- Scan multiple target with single command.
- Used to quickly identify open ports for multiple target.

### 📷 Output:

![Multiple Target Scan](screenshots/multiple-target-scan.png)

---

### 🔹 Command 4 : Scan Entire Network

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.0/24-red)

### 📌 Description:

- Scan enitre network.
- Used to quickly identify open ports for entire network.

### 📷 Output:

![Entire Network Scan](screenshots/entire-network-scan.png)

---

### 🔹 Command 5 : Specific Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--p%2080%20192.168.198.129-red)

- Scan and display single open port.
  
### 📷 Output:

![Specifi port Scan](screenshots/specific-port-scan.png)

---

### 🔹 Command 6 : Multiple Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--p%2021,22,80%20192.168.198.129-red)

- Scan and display only specified open ports.
  
### 📷 Output:

![Multiple port Scan](screenshots/multiple-port-scan.png)

---

### 🔹 Command 7 : All Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--p--%20%20192.168.198.129-red)

- Scan and display all open ports.
  
### 📷 Output:

![All port Scan](screenshots/all-port-scan.png)

---

### 🔹 Command 8 : Fast Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--F%20%20192.168.198.129-red)

- Scan and display top 100 open ports.
- Faster but less detailed.
  
### 📷 Output:

![Fast port Scan](screenshots/fast-port-scan.png)

---

### 🔹 Command 9 : OS Detection scan

![Nmap](https://img.shields.io/badge/nmap%20--O%20192.168.198.129-red)

### 📌 Description:

- Attempts to identify the operating system.
- Perform port scanning with operating system detection.
- Attackers perform os detections scan so that they can find specific exploit related to that os and service version.

### 📷 Output:

![Os Scan](screenshots/os-scan.png)

---

### 🔹 Command 10 : Aggressive Scan

![Nmap](https://img.shields.io/badge/nmap%20--A%20192.168.198.129-red)

### 📌 Description:

- Performs OS detection, version detection,traceroute, and script scanning.

### 📷 Output:

![Aggressive Scan](screenshots/aggressive-scan.png)

---

### 🔹 Command 11 : Skip Ping Scan

![Nmap](https://img.shields.io/badge/nmap%20192.168.198.129%20--Pn-red)

### 📌 Description:

Performs OS detection, version detection, and script scanning.

### 📷 Output:

![Aggressive Scan](screenshots/aggressive-scan.png)

---

### 🔹 Command 2 : Stealth Scan (SYN Scan)

![Nmap](https://img.shields.io/badge/nmap%20--sS%20192.168.198.129-red)

### 📌 Description:

- Performs half-open scan and doesn't complete TCP hanshake
- Performs a stealth scan that is less detectable.
- More stealthy than basic scan.
- Output will be the same as basic scan, displays all open ports with running service with that port.

### 📷 Output:

![Basic Scan](screenshots/syn-scan.png)

---

### 🔹 Command 3 : Service Version Detection scan

![Nmap](https://img.shields.io/badge/nmap%20--sV%20192.168.198.129-red)

### 📌 Description:

- Performs port scan with service version detection.
- Scans 1000 common ports and service with service's version.
- Attackers can find exploit based on service versions.
- Outdated services can be vulnerable and can be exploited.

### 📷 Output:

![Version Scan](screenshots/version-scan.png)

---



### 🔹 Fast Scan:

nmap -F <target>

---

## 🧠 Chapter 7: Nmap Scripts (NSE)

### 🔹 Command:

nmap --script vuln <target>

### 📌 Description:

Runs vulnerability detection scripts.

---

## 🧠 Chapter 8: Saving Output

### 🔹 Command:

nmap -oN output.txt <target>

### 📌 Description:

Saves scan results to a file.

---

## 🧠 Key Learnings

* Network reconnaissance techniques
* Different types of scanning methods
* Importance of service and OS detection

---

## ⚠️ Disclaimer

This project is for educational purposes only.
