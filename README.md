# Project-3
ed Team phishing simulation using Zphisher + Nginx + custom domain
# 🛡️ Phishing Simulation Lab: Zphisher + Nginx + Custom Domain

> 🎯 Simulating a phishing attack with a legit-looking domain using Nginx reverse proxy and Zphisher — built for red team training and detection analysis.

---

## 📌 Project Overview

This project sets up a phishing lab using:
- **Zphisher** to create fake login pages
- **Nginx** to proxy a custom domain like `login.microsoft-support.com`
- **Manual or spoofed DNS redirection** to trick victim browsers
- **Windows victim** on the same network for testing

This lab is ideal for red team portfolio, CEH practice, or setting up detection rules in Wazuh/Splunk.

---

## 🧰 Tools Used

| Tool            | Use Case                                  |
|------------------|--------------------------------------------|
| Kali Linux       | Attacker host (Zphisher + nginx)          |
| Zphisher         | Phishing page generation                  |
| Nginx            | Reverse proxy for clean domain masking    |
| Windows 10       | Victim machine on same virtual network    |
| Ettercap (optional) | DNS spoofing without victim access     |

---

## 🏗️ Lab Setup

### 🔹 Kali Linux (Attacker)
- IP: `192.168.0.104`
- Zphisher running on: `127.0.0.1:8080`
- nginx serves custom domain: `http://login.microsoft-support.com`

### 🔹 Windows 10 (Victim)
- Hosts file manually points domain to attacker's IP:
