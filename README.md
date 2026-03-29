# metasploit
# 🔐 Network Scanning using Metasploit (CEH Module 3)

This lab demonstrates how to perform network scanning, host discovery, and OS detection using Metasploit Framework integrated with Nmap.

---

## 📌 Objectives

* Scan a target network to identify active hosts
* Discover open ports and running services
* Perform SYN and TCP port scanning
* Identify operating systems of target machines

---

## 🛠 Tools Used

* Kali Linux
* Metasploit Framework
* Nmap

---

## 🔍 Steps Performed

### 1. Start Metasploit and Database

```bash
service postgresql start
msfconsole
db_status
```

---

### 2. Network Scanning using Nmap

```bash
nmap -Pn -sS -A -oX Test 10.10.1.0/24
db_import Test
```

---

### 3. Host and Service Discovery

```bash
hosts
services
```

---

### 4. SYN Port Scanning

```bash
use auxiliary/scanner/portscan/syn
set INTERFACE eth0
set PORTS 80
set RHOSTS 10.10.1.5-23
set THREADS 50
run
```

---

### 5. TCP Port Scanning

```bash
use auxiliary/scanner/portscan/tcp
hosts -R
run
```

---

### 6. OS Detection using SMB

```bash
use auxiliary/scanner/smb/smb_version
set RHOSTS 10.10.1.5-23
run
```

---

## 📊 Key Learnings

* Identified active hosts in a network
* Discovered open ports and services
* Performed port scanning using Metasploit modules
* Detected OS using SMB version scanning

---

## 🚀 Outcome

This lab improved my understanding of real-world network scanning techniques used in penetration testing and ethical hacking.

---

## 📁 Files Included

* Screenshots of scanning results
* Commands used
* Observations

---

⚡ Part of my Certified Ethical Hacker (CEH) hands-on practice.
