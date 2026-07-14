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

The following copmmands were executed to explore Linux commands.

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

A text file (abc) was created and edited using several commands.

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





