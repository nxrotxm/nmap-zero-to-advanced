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
