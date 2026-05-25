# 🔍 Python Port Scanner

A lightweight Python CLI tool that scans the 20 most common ports on any target and identifies open services. Built from scratch using only Python's standard library — no external dependencies.

Tested live on `scanme.nmap.org` — found port 22 (SSH) and port 80 (HTTP) open.

---

## ✨ Features

| Feature | Details |
|---|---|
| **20 Common Ports** | Scans SSH, HTTP, HTTPS, FTP, MySQL, RDP, MongoDB, Redis, and more |
| **Service Detection** | Labels each open port with its service name |
| **Hostname Resolution** | Accepts both IP addresses and domain names |
| **Timestamped Output** | Shows scan start time and total open ports found |
| **No Dependencies** | Uses only Python's built-in `socket` library |

---

## ⚙️ How It Works

```
Target (IP or hostname)
        │
        ├── Resolve hostname → IP address
        ├── Try TCP connection on each of 20 ports
        │       ├── Connection succeeds → Port OPEN
        │       └── Connection fails   → Port CLOSED
        │
        └── Print results + summary
```

The core logic uses `socket.connect_ex()` — if it returns `0`, the port is open.

---

## 🚀 Quick Start

### 1. Clone the repo

```bash
git clone https://github.com/kiranmai-j/python-port-scanner.git
cd python-port-scanner
```

### 2. Run the scanner

```bash
python port_scanner.py
```

### 3. Enter a target when prompted

```
Enter target IP or hostname: scanme.nmap.org
```

---

## 📊 Sample Output

```
=============================================
 Port Scanner — Target: 45.33.32.156
 Started: 2025-12-01 10:45:12
=============================================
 [OPEN] Port 22     — SSH
 [OPEN] Port 80     — HTTP
=============================================
 Scan complete. 2 open port(s) found.
=============================================
```

---

## 🗂️ Ports Scanned

| Port | Service |
|------|---------|
| 21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 135 | RPC |
| 139 | NetBIOS |
| 143 | IMAP |
| 443 | HTTPS |
| 445 | SMB |
| 3306 | MySQL |
| 3389 | RDP |
| 5900 | VNC |
| 8080 | HTTP-Alt |
| 8443 | HTTPS-Alt |
| 27017 | MongoDB |
| 5432 | PostgreSQL |
| 6379 | Redis |

---

## 🛠️ Requirements

- Python 3.x
- No external libraries needed

---

## 🔒 Disclaimer

Only scan systems you own or have explicit permission to scan. Unauthorized port scanning is illegal in many countries.

---

## 👤 Author

**Kiranmai Jorrigala**  
Cybersecurity Associate | SOC Analyst (Seeking Entry-Level)  
📧 kkiranmai216@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/kiranmai-j)

---

## ⭐ If you find this useful, give it a star!
