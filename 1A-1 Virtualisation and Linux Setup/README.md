# 1A-1 Virtualisation and Linux Setup

## Overview

This task was to set up a Linux environment and Ubuntu was installed on a virtual machine so it could be used to compelete the tasks assigned.

--- 

## Objectives

The aim of this activity was to:

- Install a VirtualBox (VMware Workstation)
- Download Ubuntu
- Create a Virtual Machine and install Ubuntu on the Virtual Machine
- Configure network settings
- Verify that Ubuntu is working

---

## Deliverables

### 1. VMware Workstation installed

VMware Workstation was installed.

<img width="2559" height="1439" alt="image" src="https://github.com/user-attachments/assets/0c83f5ff-59ff-4d97-aa26-367adbb50cdf" />

---

### 2. Ubuntu ISO Downloaded

The Ubuntu ISO was downloaded from the official Ubuntu Website.

<img width="403" height="499" alt="image" src="https://github.com/user-attachments/assets/ae6e242d-ee66-49af-87e4-2f436f5fbbaf" />

---

### 3. New Virtual Machine Created

The new VM was created with the required settings and the Ubuntu ISO was configured before installation.

<img width="750" height="721" alt="image" src="https://github.com/user-attachments/assets/85b7d410-335f-40a4-b79b-93732f24ba77" />

---

### 4.Ubuntu Installation Completed

Ubuntu was installed successfully and booted into the desktop after restarting the VM.

<img width="2559" height="1439" alt="image" src="https://github.com/user-attachments/assets/afc807a6-5d52-4fd4-9871-7d5b56b9d5bd" />

---

### 5. Network Configured

The VM was configured using NAT.

<img width="750" height="725" alt="image" src="https://github.com/user-attachments/assets/f2588ad4-55aa-40be-85f3-5ee2ed2a8758" />

---

### 6. Ubuntu Running

Ubuntu is successfully running and the terminal was accessible.

<img width="2326" height="1347" alt="image" src="https://github.com/user-attachments/assets/e7cdb2b7-c8ab-4e4e-a46f-614be7c3933e" />

---

### 7. VirtualBox Guest Additions Installed (Optional)

Virtual Box Guest additions were installed 

Commands used:

```bash
sudo apt update
sudo apt install virtualbox-guest-utils virtualbox-guest-x11
```
<img width="1131" height="1077" alt="image" src="https://github.com/user-attachments/assets/aed1b558-b80f-462b-8d59-af1c76fd326c" />

---

### 8. SSH Enabled (Optional)

OpenSSH Server was installed so the VM can be accessed remotely.

Commands used:

```bash
sudo apt install openssh-server
sudo systemctl status ssh
```

<img width="1101" height="1221" alt="image" src="https://github.com/user-attachments/assets/9a874cb5-865f-4c57-88e0-2c2385ee141d" />

Command to verify SSH is working:

<img width="1047" height="257" alt="image" src="https://github.com/user-attachments/assets/52e811d7-0160-4d0c-ab8f-5468100577f1" />

```bash
sudo systemctl status ssh.socket
```

---

## Conclusion

Ubuntu was successfully installed and configured in VMware Workstation.
