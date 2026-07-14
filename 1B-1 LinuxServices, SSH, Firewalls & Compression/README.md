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
