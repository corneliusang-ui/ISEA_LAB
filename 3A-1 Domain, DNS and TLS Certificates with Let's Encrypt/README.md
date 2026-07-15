# Domain, DNS and TLS Certificates with Let's Encrypt

## Overview

This lab introduces students to setting up a complete Internet-facing web presence. Students will configure a cloud VM, purchase and link a domain name, set DNS records, and secure their site with HTTPS using Let's Encrypt. The goal is to empower students to create real online services with full contro

# Activity 1: Domain Name Configuration

## 1. Domain Name Registered

A Domain name was registered on DuckDNS.

<img width="1062" height="896" alt="image" src="https://github.com/user-attachments/assets/ebb33e84-a8cf-45fb-bbcb-28a85b0d583a" />

---

## 2. A Record Created

A record was configured to point the domain name to EC2 public IPv4 address

<img width="600" height="119" alt="image" src="https://github.com/user-attachments/assets/075f8820-0ad9-4309-9a2b-f7ac13dfcb59" />

## 3. Apache Installed

Apache2 has been installed in the earlier labs.

To verify that Apache is running:

```bash
sudo systemctl status apache2
```

<img width="1064" height="461" alt="image" src="https://github.com/user-attachments/assets/b5070508-e497-4310-939c-7c5eeab71348" />

---

## 4. Public IP to Domain Mapping Verified

Tested using nsloopup,dig and browser to verify that DNS is working

### Commands used

```bash
nslookup corneliusisea.duckdns.org

dig corneliusisea.duckdns.org
```

The returned IP matches the EC2 public IPv4 address.

<img width="862" height="484" alt="image" src="https://github.com/user-attachments/assets/69289697-
491a-411a-bca9-7ae733208815" />

<img width="250" height="157" alt="image" src="https://github.com/user-attachments/assets/0d8b0614-c3ef-4fb9-bc91-c500b930ba7c" />

---

## 5. Apache Welcome Page via Domain

Apache was successfully accessed using the domain

https://corneliusisea.duckdns.org

<img width="859" height="1263" alt="image" src="https://github.com/user-attachments/assets/285d1d86-bced-410b-9990-4adb693b351a" />

---

## 6. DNS Test Output

Output of nslookup yourdomain.com or dig

<img width="740" height="526" alt="image" src="https://github.com/user-attachments/assets/783d4832-d681-45d5-8ebb-09ca85937460" />

---

# Activity 2: Let's Encrypt TLS Certificate Setup

## 1. Certbot Installed

Certbot and Apache plugin installed via Snap.

### Commands used

```bash
sudo snap install core
sudo snap refresh core

sudo snap install --classic certbot

sudo ln -s /snap/bin/certbot /usr/bin/certbot
```

<img width="701" height="183" alt="image" src="https://github.com/user-attachments/assets/62193763-c1b0-455d-b000-aea42d382322" />

---

## 2. HTTPS enabled on Domain

Domain shows lock icon

<img width="812" height="351" alt="image" src="https://github.com/user-attachments/assets/68b8cb82-257f-4f02-a9b7-98864be902b3" />

https://corneliusisea.duckdns.org

---

## 3. Valid TLS Certificate

Certificate was issued by Let's Encrypt

---

## 4. HTTPS with Lock Icon

Browser screenshot showing lock and certificate issuer.

<img width="894" height="1250" alt="image" src="https://github.com/user-attachments/assets/bbb181e2-5863-4ddc-b031-02c00ea352f4" />

---

## 5. Certbot Success

Output of sudo certbot --apache command.

<img width="1062" height="546" alt="image" src="https://github.com/user-attachments/assets/33e079fc-d291-4bdd-b4ba-8115429b6548" />

---

## 6. Renewal Dry-run Output

Output of sudo certbot renew --dry-run showing success.

<img width="754" height="222" alt="image" src="https://github.com/user-attachments/assets/8969a5b8-a31d-4ff7-a8a1-82d6521a20e1" />

---

# Reflection

This activity demonstrated how DNS allows a human-readable domain name to be mapped to an IP address, making web servers easier to access than by using numerical IP addresses. Configuring DNS records and verifying them with tools such as `nslookup` and `dig` helped reinforce how domain name resolution works.

The activity also introduced HTTPS by securing the website with a free TLS certificate issued by Let's Encrypt. Using Certbot simplified the installation and configuration process, while the renewal dry-run demonstrated how certificate maintenance can be automated. These are essential skills for deploying secure, publicly accessible web services in cloud environments.
