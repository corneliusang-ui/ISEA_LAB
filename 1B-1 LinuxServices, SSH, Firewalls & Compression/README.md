# 1B-1: Linux Services, SSH, Firewalls & Compression

## Overview

This objective introduces set up and explore Apache, SSH, and UFW firewall services in Ubuntu, perform port scanning and file transfer over SSH, and practice compression and decompression using tar, bzip2, and scp. 

For this Objective, I have no partner so everything is done on my own machine.

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

For this deliverable, I used my own webpage as I do not have a partner

<img width="1010" height="591" alt="image" src="https://github.com/user-attachments/assets/d5bbd9c3-98f7-4564-b71f-9e5c31049547" />

## 4. Nmap Port Scan Results

Nmap was used to scan my own machine.

Commands used:

```bash
sudo apt install nmap
nmap localhost
```

<img width="1117" height="1105" alt="image" src="https://github.com/user-attachments/assets/5904e694-f4c0-45da-bb7f-482257c91b40" />

---

## 5. Firewall (UFW) Status and Rules

The Ubuntu Firewall was confirgured to allow HTTP traffic.

Commands used:

```bash
sudo ufw status verbose
sudo ufw enable
sudo ufw allow 80/tcp
sudo ufw status verbose
nmap 172.17.0.1
```

The firewall configuration was verified using nmap scan.

<img width="1014" height="202" alt="image" src="https://github.com/user-attachments/assets/4408eef4-4f21-4b47-b23c-426a2e90372a" />

---

## 6. SSH Enabled and Tested

SSH was enabled to allow secure remote login.

Commands used:

```bash
sudo systemctl enable ssh
sudo systemctl start ssh
whoami
ssh localhost
```

A login attempt was achieved using my own machine.

<img width="1093" height="307" alt="image" src="https://github.com/user-attachments/assets/e25826ef-e4f0-463c-9986-5eb65e52d5b1" />

---

## 7. New User Created and verified

Created a new linux user.

Commands used:

```bash
sudo adduser testuser

grep testuser /etc/passwd
```

The new user entry was verified inside '/etc/passwd'.

<img width="1049" height="324" alt="image" src="https://github.com/user-attachments/assets/191fb590-f366-433f-9a0b-67b8df86f8df" />

---

## 8. Compression and Decompression Tested

Files were archived using compression and tar using bzip2

Commands used:

```bash
tar cf backup.tar folder/

bzip2 backup.tar

bunzip2 backup.tar.bz2

tar -xvf backup.tar

ls-lah
```

Comparison of the before and after of archive size.

<img width="1024" height="511" alt="image" src="https://github.com/user-attachments/assets/6ddf277f-7817-4f11-b20f-7c7bf94089c0" />

---

## 9. SCP File Transfer between machines

As I do not have a partner, I created and transfered files within my own machine.

Commands used:

```bash
touch test.txt
scp test.text cornelius@localhost:~/copied-test.txt 
mkdir testfolder
scp -r testfolder cornelius@localhost:~/
ls ~
```

<img width="1110" height="307" alt="image" src="https://github.com/user-attachments/assets/8f84ec9b-2833-41ae-bd9d-ca3d31f29fde" />

---

## Deliverables 10-14 have been completed in Assignment 1A-2

https://github.com/corneliusang-ui/ISEA_LAB/blob/main/1A-2%20Ubuntu%20Desktop%20and%20Command%20Line%20Familiarisation/README.md

---

# Conclusion 

This objective provided practical experience with Apache web server administration, Linux networking, firewall configuration, SSH, secure file transfer, compression, DNS utilities and system administration. Completing these activities improved my confidence in configuring Linux servers and communicating between multiple Ubuntu systems.












