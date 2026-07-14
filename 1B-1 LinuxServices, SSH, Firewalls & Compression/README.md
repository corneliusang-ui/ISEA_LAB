# 1B-1: Linux Services, SSH, Firewalls & Compression

## Overview

This objective introduces set up and explore Apache, SSH, and UFW firewall services in Ubuntu, perform port scanning and file transfer over SSH, and practice compression and decompression using tar, bzip2, and scp. 

---

# Deliverables

## 1. Apache Web Server Installed

Apache Web Server was installed using the APT package manager.

Commands used:

```bash
sudo apt update
sudo apt install apache2
sudo systemctl status apache2
```

Verification:

```
http://127.0.0.1
```
<img width="2277" height="1310" alt="image" src="https://github.com/user-attachments/assets/2bb6dbc9-4677-4b18-9057-cfc22a4360e5" />

---

## 2. Modified index.html Page

The default Apache homepage was replaced with a personalised webpage.

Commands used:

```bash
sudo nano /var/www/html/index.html
```
The webpage was then accessed through the browser.

<img width="1069" height="638" alt="image" src="https://github.com/user-attachments/assets/d82e2acc-d867-4abe-af9e-c0263e7c6dc8" />

---

## 3. IP Address Identified and Shared

The Network configuration was displayed to identify the loopback and local IP address.

Command used:

```bash
ip a
```

