# Ubuntu Desktop and Command Line Familiarisation

## Overview

This session introduces students to the Ubuntu Desktop and emphasises command-line use. Students will explore file navigation, permissions, network tools, user management, and software installation via GUI and CLI. 

---

## Objective

- Understand the Ubuntu desktop and basic command-line interface (CLI). 
- Use basic terminal commands for navigation, file handling, and user management. 
- Explore system information, process monitoring, and networking tools. 
- Understand software installation via GUI, APT, and source compilation. 
- Compare public/private IPs and experiment with host configuration. 
- Develop beginner C program and compile using GCC. 

---

## Deliverables

### 1. GUI Familiarisation

Firefox was opened to verify internet connectivity.

<img width="1141" height="883" alt="image" src="https://github.com/user-attachments/assets/23796ee9-91f2-43b7-ad3a-56f01e170c4b" />

LibreOffice Writer was opened with text typed.

<img width="2256" height="1289" alt="image" src="https://github.com/user-attachments/assets/78363d0d-eda3-4afc-92a9-d89fc3447e68" />

The Ubuntu File manager navigating directories.

<img width="879" height="537" alt="image" src="https://github.com/user-attachments/assets/3ebe4aa0-b1ec-433c-a1bd-b191283eeab6" />

Ubuntu Software was opened and used to install gitea

<img width="1323" height="847" alt="image" src="https://github.com/user-attachments/assets/fc28f493-8b4c-413b-bb31-2b52ddeb2be0" />

---

### 2. Terminal Commands Output

The following commands were executed to explore Linux commands.

```bash
ps -e
top
ls
ls -la
ls -alt
```

Output for ps -e:

<img width="1128" height="1236" alt="image" src="https://github.com/user-attachments/assets/9c6a6e75-0126-4006-940b-2a05c36d8ecc" />

Output for top:

<img width="1121" height="1252" alt="image" src="https://github.com/user-attachments/assets/ce6b27af-4ecb-4746-a711-129ffa4ae8fe" />

Output for ls, ls-la & ls -alt:

<img width="1072" height="346" alt="image" src="https://github.com/user-attachments/assets/c5493745-86a7-4fea-a625-eecaa7d6eb0a" />

#### File creation and editing

A text file (abc.txt) was created and edited using several commands.

Creating the file:

```bash
touch abc.txt
```

<img width="1023" height="484" alt="image" src="https://github.com/user-attachments/assets/7f031c9f-4581-4b48-9955-a6cbc2dcba93" />

Editing the file:

```bash
nano abc.txt
gedit abc.txt
```

<img width="1134" height="1064" alt="image" src="https://github.com/user-attachments/assets/f7282b83-544a-4fee-8af5-46fa0b0d2159" />

Displaying the contents:

```bash
cat abc.txt
```

<img width="904" height="38" alt="image" src="https://github.com/user-attachments/assets/824474d4-b997-47ac-8b04-b2448c4d5ed9" />

Viewing the file one page at a time:

```bash
less myfile.txt
```

<img width="1137" height="1278" alt="image" src="https://github.com/user-attachments/assets/22cce7b3-e4f3-481a-86ed-ca8de973b793" />

---

### 3. File Operations

Files were copied, renamed and removed.

Commands used:

```bash
cp abc.txt copy.txt
mv copy.txt abcd.txt
rm abcd.txt
ls -lah
```

Copying abc.txt to copy.txt:

<img width="931" height="445" alt="image" src="https://github.com/user-attachments/assets/458642ed-5fa3-4922-bb70-1c3b9a6c6514" />

Renaming copy.txt to abcd.txt:

<img width="920" height="456" alt="image" src="https://github.com/user-attachments/assets/fa598a8a-7e3c-436c-9647-55ddd5e2fbb6" />

Command to delete abcd.txt from folder:

```bash
rm abcd.txt
```

Command to make sure abcd.txt is no longer in files:

```bash
ls -lah
```

<img width="634" height="164" alt="image" src="https://github.com/user-attachments/assets/ac0e81e0-dd70-4340-a754-74ee70283b79" />

### 4. System Information Commands

The commands below used were used to obtain information of the Operating System (OS) and hardware.

Commands used:

```bash
uname -a
lsb_release -a
hostnamectl
cat /proc/cpuinfo
```

Command Explanations:

-'uname -a' displays kernal information
-'lsb_release -a' displays Ubuntu version
-'hostnamectl' displays system hostname and OS information
-'cat /proc/cpuinfo' displays CPU information

<img width="1115" height="1206" alt="image" src="https://github.com/user-attachments/assets/6430db38-c9a4-4c7d-9c42-2509b1eab555" />

---

### 5. User Privilege Experiment

This deliverable shows the differences between a normal user and administrator (root) user.

Commands Used:

```bash
whoami
sudo whoami
adduser testuser
sudo adduser testuser
```

Observation:

Attempting to add user without sudo results in a permission error. Only when using 'sudo' infront will then allow the user to add a user.

<img width="738" height="296" alt="image" src="https://github.com/user-attachments/assets/98c4f9fe-49b5-4fe5-a335-d12bf09d5ed0" />

---

### 6. Networking Tests

Network commands were executed to verify network connections.

Commmands used:

```bash
ip a
ping 8.8.8.8
```

<img width="1112" height="421" alt="image" src="https://github.com/user-attachments/assets/8ef85f67-d5e9-4d0d-b701-58b6bd792ee8" />


Screenshot of Ubuntu network settings window:

<img width="960" height="617" alt="image" src="https://github.com/user-attachments/assets/7fef1443-86df-4912-ae6f-a73ed079cb3b" />

---

### 7. Editing /etc/hosts file

Nano was used to create a custom hostname.

Commands used:

```bash
sudo nano /etc/hosts
```

```text
8.8.8.8 GoogleEpicDNS
```

<img width="1128" height="221" alt="image" src="https://github.com/user-attachments/assets/8449bd9b-53bc-499a-ba27-5b6ed43854ea" />

Testing the hostname:

```bash
ping GoogleEpicDNS
```

<img width="853" height="140" alt="image" src="https://github.com/user-attachments/assets/d862c621-4cd9-418e-a0e2-a4fcf2224915" />

---

### 8. DNS lookup performed

DNS lookup was used to retrieve domain infomation.

Commands used:

```bash
nslookup google.com
whois google.com
```

DNS records and domain registration information was displayed.

<img width="1109" height="1226" alt="image" src="https://github.com/user-attachments/assets/1ae26607-37cd-4858-ba8f-fb82be0fc8e6" />

---

### 9. Public vs Private IP Reflection

Private IP was obtained using:

```bash
ip a
```

<img width="1027" height="309" alt="image" src="https://github.com/user-attachments/assets/73d4f5f4-dd04-4183-a110-ab7901f4298a" />

The public IP was obtained from:

https://whatismyipaddress.com

<img width="1023" height="741" alt="image" src="https://github.com/user-attachments/assets/12ca9069-255b-4922-8e14-99af5abc503b" />

Difference:

The private IP address is only used within local network and cannot be directly accessed from the Internet whereas Public IP address is assigned by the Internet Service Provider which is used for internet usage.

### 10. Hardware Information Commands

Hardware information was used to compare with Ubuntu's graphical system information.

Commands used:

```bash
lsusb
lspci
less /proc/cpuinfo
```

Ubuntu settings was used for comparison.

lsusb & lspci output:

<img width="1095" height="970" alt="image" src="https://github.com/user-attachments/assets/0af53f8c-ed20-4b67-9fcb-72b74172c1f9" />

less /proc/cpuinfo output:

<img width="1120" height="1243" alt="image" src="https://github.com/user-attachments/assets/da79720e-1f01-43d6-9ba7-f28ef646d8f6" />

Ubuntu system information:

<img width="962" height="625" alt="image" src="https://github.com/user-attachments/assets/896d05b6-63e4-4f14-9b3c-4becf1aaf5db" />

---

### 11. Output Redirection

Output redirection was used to practice command output into a file.

Commands used:

```bash
lsusb > output_of_lsusb
cat output_of_lsusb
less output_of_lsusb
rm output_of_lsusb
```
lsusb > output_of_lsusb, cat output_of_lsusb & rm output_of_lsusb output:

<img width="1109" height="260" alt="image" src="https://github.com/user-attachments/assets/4ed49ad9-5d52-492d-9654-203d91017d90" />

less output_of_lsusb output:

<img width="1110" height="1276" alt="image" src="https://github.com/user-attachments/assets/bdb18d76-0c00-40c4-b620-5d02eaa0ef1b" />

This demonstrates how Linux can redirect command output into a txt file.

---

### 12. Software Installed (3 Ways)

3 Different software installation methods were used.

#### SaaS

A cloud based application accessed through Firefox.

Google Docs was used:

<img width="1097" height="877" alt="image" src="https://github.com/user-attachments/assets/146286b8-5085-4f8c-a50f-92a3c97fbda1" />

---

#### Binary Installation

A .deb file (Chrome) on was downloaded and installed.

```bash
sudo dpkg -i google-chrome-stable_current_amd64.deb
```
.deb file:

<img width="765" height="517" alt="image" src="https://github.com/user-attachments/assets/3e0d77eb-f2ba-4696-8a5c-68e31938d6b3" />

Chrome installed:
<img width="1086" height="1114" alt="image" src="https://github.com/user-attachments/assets/0d5193ce-4960-4007-80d3-c6406e15541f" />

#### Repository Installation

Software was installed via Ubuntu Software Centre.

Application installed was VLC

<img width="1302" height="845" alt="image" src="https://github.com/user-attachments/assets/27a99742-45d9-4a4b-9e82-26577135ee36" />

---

### 13. Command-Line Install via apt

Commands used:

```bash
sudo apt update
sudo apt upgrade
sudo apt install vlc
```

Optional:

```bash
less /etc/apt/sources.list
```

These commands update the package information, upgrade installed packages and install new software.

sudo apt update sudo apt upgrade outputs:

<img width="1141" height="1200" alt="image" src="https://github.com/user-attachments/assets/b6fceb24-dba4-4bcb-90cb-60fca9113bb3" />

sudo apt install vlc output:

<img width="784" height="238" alt="image" src="https://github.com/user-attachments/assets/243d2181-1ff8-41dc-9f75-fe7a1c4d2dee" />

less /etc/apt/sources.list output:

<img width="1121" height="1275" alt="image" src="https://github.com/user-attachments/assets/b1eb95ab-e38c-45a2-b1b4-0a8285685f90" />

---

### 14. Source Code Compliation

A C program was created, compiled and executed.

Source file was created in notes app.

Source file:

```c
#include <stdio.h>

int main()
{
  printf("Hello World!\n");
  return 0;
}
```

<img width="684" height="514" alt="image" src="https://github.com/user-attachments/assets/cac0fbd3-e85e-47d6-913d-d1676a81c3d7" />

Compilation:

```bash
gcc hello_world.c -o hello_world_executable
```

Execution:

```bash
./hello_world_executable
```

If permission denied:

```bash
chmod 777 hello_world_executable
```

Program output:

```text
Hello World!
```

Compilation & Execution output:

<img width="856" height="102" alt="image" src="https://github.com/user-attachments/assets/efaf044d-7ba4-405c-9665-01fbb3395c34" />

---

## Conclusion

This Assignment provided practical experiences with Ubuntu Desktop and the Linux command line.






















