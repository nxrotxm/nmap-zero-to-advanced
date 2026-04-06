# 📘 Chapter 1: Introduction to Network Scanning & Ethical Hacking

---

## 🧠 What is Ethical Hacking?

Ethical hacking is the practice of testing systems, networks, and applications to find **security weaknesses** — legally and with proper authorization.

### ✅ Ethical hackers:

- ⚖️ Follow the law  
- 🔑 Work with permission  
- 🛡️ Help organizations improve security  

---

## 🎯 Why Network Scanning Matters

Before exploiting a system, you must first **understand it**.

Network scanning is the **first step in hacking**, used to:

- 🖥️ Discover live systems  
- 🔓 Identify open ports  
- 🧭 Detect running services  
- 🎯 Map the attack surface  

---

## 🏠 Real-World Analogy

Think of a target network like a house:

| Concept        | Real World Example |
|---------------|------------------|
| 🌐 IP Address | House address |
| 🚪 Ports      | Doors & windows |
| 🛠️ Services   | What’s inside the rooms |

👉 **Scanning = Checking which doors/windows are open**

---

## 🔗 Phases of Ethical Hacking

Every penetration test follows a structured process:

---

### 1️⃣ Reconnaissance (Information Gathering)
- Collect target information  
- Domain, IP, employees  

---

### 2️⃣ Scanning ✅ *(Your Focus)*
- Find live hosts  
- Identify open ports  
- Detect services  

---

### 3️⃣ Enumeration
- Extract deeper information  
- Users, versions, shares  

---

### 4️⃣ Exploitation
- Use vulnerabilities to gain access  

---

### 5️⃣ Post-Exploitation
- Maintain access  
- Extract sensitive data  

---

### 6️⃣ Reporting
- Document findings  
- Provide remediation steps  

---

## ⚡ Summary

- 🧠 Ethical hacking = Legal security testing  
- 🔍 Scanning = First technical step  
- 🎯 Goal = Understand target before attack  

---

## ⚙️ What is Nmap?

**Nmap (Network Mapper)** is a powerful open-source tool used for:

- 🌐 Network discovery  
- 🔓 Port scanning  
- 🧭 Service detection  
- 🛡️ Vulnerability scanning  

---

## 🔥 Why Hackers Love Nmap

- ⚡ Fast and flexible  
- 🕵️ Supports stealth scanning  
- 🧩 Powerful scripting engine (NSE)  
- 💻 Works on almost all platforms  

---

## ⚠️ Legal Warning (IMPORTANT)

🚨 **Never scan systems without permission.**

Unauthorized scanning can:

- ⛔ Get you banned  
- ⚖️ Lead to legal action  
- 💣 Be considered a cyber attack  

---

## 🧪 Real-World Scenario

Imagine:

You are hired to test a company’s network.

Before doing anything:

- 🔍 You run scans  
- 🧭 Identify open services  
- 🎯 Look for weaknesses  

➡️ **Without scanning, you are blind**

---

# 📘 Chapter 2: Networking Basics for Hackers

---

## 🌐 Why Networking Knowledge is Critical

You cannot be a good hacker without understanding how networks work.

🧠 Nmap is not magic — it relies on:
- 📡 Protocols  
- 📦 Packets  
- 📜 Communication rules  

---

## 🧠 What is a Network?

A **network** is a group of devices connected to share data.

### Examples:
- 📶 Wi-Fi network  
- 🏢 Office network  
- 🌍 Internet  

---

## 🆔 IP Address (Identity of a Device)

An IP address is like a **unique ID** for a device.

---

## 🔎 Types of IP Addresses

### 🟢 Private IP
- Used inside local networks  
- Examples:
- 192.168.x.x
- 10.x.x.x


### 🔴 Public IP
- Visible on the internet  
- Assigned by ISP  

---

## 🚪 What is a Port?

A **port** is a communication endpoint.

👉 One device can run multiple services using different ports.

---

## 📊 Common Ports

| Port | Service | Description |
|------|--------|------------|
| 21   | FTP    | File transfer |
| 22   | SSH    | Remote login |
| 23   | Telnet | Insecure remote access |
| 25   | SMTP   | Email sending |
| 53   | DNS    | Domain resolution |
| 80   | HTTP   | Web traffic |
| 443  | HTTPS  | Secure web |

---

## 🚦 Port States (VERY IMPORTANT)

- 🟢 **Open** → Service is running  
- 🔴 **Closed** → No service  
- 🟡 **Filtered** → Firewall blocking  

---

## 📡 Protocols: TCP vs UDP

### 🔵 TCP (Transmission Control Protocol)
- Connection-oriented  
- Reliable  

**Used in:**
- HTTP  
- SSH  
- FTP  

---

### 🔴 UDP (User Datagram Protocol)
- Connectionless  
- Faster but less reliable  

**Used in:**
- DNS  
- Streaming  
- VoIP  

---

## 🤝 TCP 3-Way Handshake

This is critical for understanding Nmap scans:

## SYN → SYN-ACK → ACK


### Step-by-step:

1. Client sends **SYN**  
2. Server replies **SYN-ACK**  
3. Client sends **ACK**  

➡️ **Connection established**

---

## 🧠 Why This Matters for Nmap

Nmap manipulates this handshake:

- ⚡ **SYN Scan** → Does NOT complete handshake (stealthy)  
- 🔍 **TCP Scan** → Completes handshake  

---

## 🔥 Firewall Basics

A **firewall**:

- 🛡️ Monitors traffic  
- 🚫 Blocks suspicious packets  

### Example:
- Blocks unknown ports  
- Filters scanning attempts  

---

## 🧪 Real-World Scenario

You scan a target and see:
- 80/tcp | open | http
- 22/tcp | filtered | ssh


### 👉 Meaning:

- 🌐 Website is accessible  
- 🔒 SSH is blocked by firewall  

---

## 🔥 You Now Have Strong Foundation

After these chapters:

- 🧠 You understand how networks work  
- 🔍 You understand how Nmap thinks  

---

# 📘 Chapter 3: Nmap Practical Scanning (Real Commands)

---

## ⚡ Introduction

Now that you understand networking basics, it's time to **use Nmap in real scenarios**.

🎯 Goal: Learn how to scan targets like a real penetration tester.

---

## 🔍 Basic Scan

