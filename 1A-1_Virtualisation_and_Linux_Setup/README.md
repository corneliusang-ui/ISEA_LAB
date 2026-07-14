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

---

### 2. Ubuntu ISO Downloaded

The Ubuntu ISO was downloaded from the official Ubuntu Website.

---

### 3. New Virtual Machine Created

The new VM was created with the required settings and the Ubuntu ISO was configured before installation.

---

### 4.Ubuntu Installation Completed

Ubuntu was installed successfully and booted into the desktop after restarting the VM.

---

### 5. Network Configured

The VM was configured using NAT.

---

### 6. Ubuntu Running

Ubuntu is successfully running and the terminal was accessible.

---

### 7. VirtualBox Guest Additions Installed (Optional)

Virtual Box Guest additions were installed 

Commands used:

```bash
sudo apt update
sudo apt install virtualbox-guest-utils virtualbox-guest-x11
```

---

### 8. SSH Enabled (Optional)

OpenSSH Server was installed so the VM can be accessed remotely.

Commands used:

```bash
sudo apt install openssh-server
sudo systemctl status ssh
```

---

## Conclusion

Ubuntu was successfully installed and configured in VMware Workstation.
