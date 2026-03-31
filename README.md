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

### 🔹 Command 1 : Basic scan/default scan

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.129-red)

### 📌 Description:

- Default scan of nmap.
- Used to quickly identify open ports.
- Scan top 1000 common ports and displays all open ports with running service with that port.

### 📷 Output:

![Basic Scan](screenshots/basic-scan.png)

---

### 🔹 Command 2 : Multiple Target scan

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.129%20192.168.198.2-red)

### 📌 Description:

- Scan multiple target with single command.
- Used to quickly identify open ports for multiple target.

### 📷 Output:

![Multiple Target Scan](screenshots/multiple-target-scan.png)

---

### 🔹 Command 3 : Scan Entire Network

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.129/24-red)

### 📌 Description:

- Scan enitre network.
- Used to quickly identify open ports for entire network.

### 📷 Output:

![Basic Scan](screenshots/basic-scan.png)

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

### 🔹 Command 4 : OS Detection scan

![Nmap](https://img.shields.io/badge/nmap%20--O%20192.168.198.129-red)

### 📌 Description:

- Attempts to identify the operating system.
- Perform port scanning with operating system detection.
- Attackers perform os detections scan so that they can find specific exploit related to that os and service version.

### 📷 Output:

![Version Scan](screenshots/os-scan.png)

---

### 🔹 Command 5 : Aggressive Scan

![Nmap](https://img.shields.io/badge/nmap%20--A%20192.168.198.129-red)

### 📌 Description:

Performs OS detection, version detection, and script scanning.

### 📷 Output:

![Aggressive Scan](screenshots/aggressive-scan.png)

---

### 🔹 Command 6 : Specific Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--p%2080%20192.168.198.129-red)

- Displays only specified open port.
- bellow is the example in screenshot.
  
### 📷 Output:

![Specifi port Scan](screenshots/specific-port-scan.png)

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
