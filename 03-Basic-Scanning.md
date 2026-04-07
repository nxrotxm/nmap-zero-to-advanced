# 📘 Chapter 3: Nmap Practical Scanning (Real Commands)

---

## ⚡ Introduction

Now that you understand networking basics, it's time to **use Nmap in real scenarios**.

🎯 Goal: Learn how to scan targets like a real penetration tester.

---

# 🔍 Basic Scan

### 🔹 Command 1 : Host Discovery scan

 ![Nmap](https://img.shields.io/badge/nmap%20--sn%20192.168.198.0/24-red)

### 📌 Description:

- Scans the entire network to identify and display live hosts.
- It does not scan ports.

### 📷 Output:

![Basic Scan](screenshots/host-discovery-scan.png)

---

### 🔹 Command 2 : Basic scan/default scan

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.129-red)

### 📌 Description:

- This is the default scan performed by Nmap.
- Scans the 1,000 most common ports.
- Scans the top 1,000 common ports and shows open ports with their running services.

### 📷 Output:

![Basic Scan](screenshots/basic-scan.png)

---

### 🔹 Command 3 : Multiple Target scan

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.129%20192.168.198.2-red)

### 📌 Description:

- Scans multiple IPs in one command.
- Used to quickly identify open ports on multiple IPs.

### 📷 Output:

![Multiple Target Scan](screenshots/multiple-target-scan.png)

---

### 🔹 Command 4 : Scan Entire Network

  ![Nmap](https://img.shields.io/badge/nmap%20%20192.168.198.0/24-red)

### 📌 Description:

- Scans all 256 IPs in a network.
- Used to quickly identify open ports for available IPs in entire network.

### 📷 Output:

![Entire Network Scan](screenshots/entire-network-scan.png)

---

### 🔹 Command 5 : Specific Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--p%2080%20192.168.198.129-red)

- Performs a scan to identify and display a single open port.
  
### 📷 Output:

![Specifi port Scan](screenshots/specific-port-scan.png)

---

### 🔹 Command 6 : Multiple Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--p%2021,22,80%20192.168.198.129-red)

- Performs a scan to identify and display only the specified open ports.
  
### 📷 Output:

![Multiple port Scan](screenshots/multiple-port-scan.png)

---

### 🔹 Command 7 : All Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--p--%20%20192.168.198.129-red)

- Scans all 65,535 ports and displays open ports.
- Useful for deep enumeration
  
### 📷 Output:

![All port Scan](screenshots/all-port-scan.png)

---

### 🔹 Command 8 : Fast Port Scan

![Nmap](https://img.shields.io/badge/nmap%20--F%20%20192.168.198.129-red)

- Performs a scan to identify and display the top 100 open ports.
- Faster, but less detailed.
  
### 📷 Output:

![Fast port Scan](screenshots/fast-port-scan.png)

---

### 🔹 Command 9 : Skip Ping Scan

![Nmap](https://img.shields.io/badge/nmap%20192.168.198.129%20--Pn-red)

### 📌 Description:

- Skips ping
- Assumes the host is up.
- This option is used when the firewall blocks ICMP packets.

### 📷 Output:

![Skip Ping Scan](screenshots/skip-ping-scan.png)

---

### 🔹 Command 10 : Save Outout

![Nmap](https://img.shields.io/badge/nmap%20--oN%20192.168.198.129%20-red)

### 📌 Description:

- Saves results for later analysis.
- There are additional options to save output. For example, -oX saves in XML format, -oG in grepable format, and -oA saves all formats at once.

### 📷 Output:

![Save Output](screenshots/save-output.png)


---
