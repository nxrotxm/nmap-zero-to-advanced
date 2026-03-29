# 🔍 Nmap Complete Guide (Beginner to Advanced)

## 📘 Introduction

Nmap (Network Mapper) is a powerful tool used for network discovery and security auditing.

---

## ⚙️ Lab Setup

* Kali Linux (Attacker)
* scanme.nmap.org (Target)

---

## 🧠 Chapter 1: Basic Scanning

### 🔹 Command:

nmap <target>

### 📌 Description:

Performs a basic scan to find open ports.

### 📷 Output:

![Basic Scan](screenshots/basic-scan.png)

---

## 🧠 Chapter 2: Stealth Scan (SYN Scan)

### 🔹 Command:

nmap -sS <target>

### 📌 Description:

Performs a stealth scan that is less detectable.

### 📷 Output:

(Add screenshot)

---

## 🧠 Chapter 3: Service Version Detection

### 🔹 Command:

nmap -sV <target>

### 📌 Description:

Detects services and their versions.

### 📷 Output:

(Add screenshot)

---

## 🧠 Chapter 4: OS Detection

### 🔹 Command:

nmap -O <target>

### 📌 Description:

Attempts to identify the operating system.

### 📷 Output:

(Add screenshot)

---

## 🧠 Chapter 5: Aggressive Scan

### 🔹 Command:

nmap -A <target>

### 📌 Description:

Performs OS detection, version detection, and script scanning.

### 📷 Output:

(Add screenshot)

---

## 🧠 Chapter 6: Port Scanning Techniques

### 🔹 Specific Ports:

nmap -p 21,22,80 <target>

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
