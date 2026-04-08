# 📘 Chapter 6: Service Enumeration & Exploitation Path

---

## 🔍 What is Enumeration?

**Enumeration** is the process of extracting **detailed information** from a target service.

- Unlike scanning (which finds ports), enumeration goes deeper.

---

### 🧠 Enumeration Answers Questions Like:

- ❓ What exactly is running?  
- 👤 Who are the users?  
- 💣 What vulnerabilities exist?  

---

## ⚔️ Scanning vs Enumeration

| Phase        | Purpose |
|-------------|--------|
| 🔍 Scanning  | Find open ports |
| 🧠 Enumeration | Extract detailed data |

---

# ⚙️ Lab Setup

## 🖥️ Attacker Machine

- Kali Linux
## 🎯 Target Machine
- Metasploitable2 IP (example): 192.168.198.129

---

# let's start enumaration and exploits

### To perform enumaration, first it's neccessery to find open port and services running on it.

### 🔹 Command 1 : Stealth Scan (SYN Scan) (Basic recon)

![Nmap](https://img.shields.io/badge/nmap%20--sS%20192.168.198.129-red)

### 📌 Description:

- By running this command, all open ports and running services will be displayed as output.

### 📷 Output:

![Basic Scan](screenshots/syn-scan.png)

🎯 All open ports are listed above. The next step is to determine the versions of the associated services.

---

### 🔹 Command 2 : Service Version Detection scan

![Nmap](https://img.shields.io/badge/nmap%20--sV%20192.168.198.129-red)

### 📌 Description:

- By running this command, all open ports and running services and versions of the associated services will be displayed as output

### 📷 Output:

![Version Scan](screenshots/version-scan.png)

🎯 All open ports and versions of the associated services listed above. The next step is to enumarate services.

---

### All the open port and services are found on a target, let's enumarate each service step-by-step 

---

# 📂 FTP Enumeration

FTP (File Transfer Protocol) is commonly found on port **21** and is often **misconfigured**, making it a valuable target.

---

## 🎯 Objective

- 🔍 Identify FTP service details  
- 🔑 Check for anonymous access  
- 📂 Discover sensitive files  
- 💣 Find potential vulnerabilities  

---

![Nmap](https://img.shields.io/badge/nmap%20--p%2021%20----script=ftp--anon%20192.168.198.129-red)

### 📌 Description:

- This command will check whether anonymous login is allowed or not.

### 📷 Output:

![Version Scan](screenshots/ftp-enum.png)

- As shown above, the FTP service is misconfigured and vulnerable as it allows anonymous login.
- An attacker can gain access to the FTP service without providing valid authentication credentials.
- vsFTPd version 2.3.4 contains a known backdoor vulnerability that can be exploited using the Metasploit framework.

### Note : Exploitation of the FTP service typically requires valid credentials or a misconfiguration.

---

# 🔐 SSH Enumaration


<p align="center">
  ⚡ “Scanning shows the door. Enumeration finds the key.” ⚡
</p>
