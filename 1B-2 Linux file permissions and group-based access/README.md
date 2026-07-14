# 1B-2 Linux File Permissions and Group-Based Access

## Overview

Demonstrate understanding of Linux file permission schemes by creating users and groups, assigning proper access rights to directories and files, and validating access control using real users and the su, chmod, and chown toolset.

---

# Deliverables

## 1. Three Users Created

Three new user accounts (alice, bob and mallory were created using 'adduser' command.

Commands used;

```bash
sudo adduser alice
sudo adduser bob
sudo adduser mallory
```

The users were verified using:

```bash
less /etc/passwd
```

<img width="807" height="56" alt="image" src="https://github.com/user-attachments/assets/3c652b68-7bd9-488a-8b18-aba2083dc038" />

---

## 2. Group Created and Configured

'sharedgroup' was created. Both alice and bob were added to the group.

Commands used:

```bash
sudo groupadd sharedgroup

sudo adduser alice sharedgroup

sudo adduser bob sharedgroup
```

The group membership was verified using:

```bash
less /etc/group
```

<img width="779" height="17" alt="image" src="https://github.com/user-attachments/assets/7daa3017-00a9-4044-8c18-8593f30cb87b" />

---

## 3. Shared Director Created in /home/

A shared director was created inside '/home' and ownership was configured. Ownership was given to alice

Commands used:

```bash
sudo mkdir /home/shared

sudo chown alice /home/shared

sudo chgrp sharedgroup /home/shared
```

Director permissions were verified using:

```bash
ls -ld /home/shared
```   

<img width="772" height="117" alt="image" src="https://github.com/user-attachments/assets/42ed9f0b-571c-47d9-93f0-4d2073211e9a" />

---

## 4. Ten Files Created in 'shared' folder

txt files were created inside the shared directory.

Command used to switch to alice:

```bash
su - alice
```

Commands used:

```bash
cd /home/shared

touch file1.txt file2.txt file3.txt file4.txt file5.txt
touch file6.txt file7.txt file8.txt file9.txt file10.txt
```

Verification:

```bash
ls -l /home/shared
```

<img width="813" height="254" alt="image" src="https://github.com/user-attachments/assets/062082ee-4425-4ed7-b625-f949d8dde2fc" />

---

## 5. Permissions Assigned Properly

Permissions were configured so that:

- alice can read, write and execute permissions.
- bob can read and execute permissions.
- mallory has no access.

Commands used:

```bash
sudo chmod -R 750 /home/shared

sudo chown -R alice:sharedgroup /home/shared
```

Verification:

```bash
ls -l /home/shared
```

<img width="743" height="71" alt="image" src="https://github.com/user-attachments/assets/571a4d34-d15f-4c7c-a520-02bc41bdf1b1" />

---

## 6. Access Verified as Each user

Access was tested using each user account

### alice

Commands used:

```bash
su - alice

whoami
```

alice was able to create, edit and delete files.

---

### Bob 

Commands used:

```bash
su - bob

whoami
```

bob was able to read files but could not modify protected files.

---

### mallory

Commands used:

```bash
su - mallory

whoami
```

mallory completely has no access to any files.

<img width="816" height="739" alt="image" src="https://github.com/user-attachments/assets/969ce1bc-9305-4d35-ace8-c6d7f5d05d81" />

---

## 7. Use of chmod/chown/chgrp-R

Recursive flag commands were used to apply ownership and permissions to all files inside the shared folder.

Commands used:

```bash
sudo chmod -R 750 /home/shared
sudo chown -R alice:sharedgroup /home/shared
sudo chgrp -R sharedgroup /home/shared
```

Verification

```bash
ls -lR /home/shared
```

<img width="825" height="394" alt="image" src="https://github.com/user-attachments/assets/184f93fc-af02-4428-8e9c-8ba7f647a54b" />

---

## 8. Mallory added to Sudoers

Mallory was granted admin privileges by adding her to the sudo group.

Commands used:

```bash
sudo usermod -aG sudo mallory
```

Verification:

```bash
groups mallory
```

<img width="748" height="88" alt="image" src="https://github.com/user-attachments/assets/a166d1ba-a1cd-4e28-9818-de4605030fc4" />

---

## 9. Effect of Sudo Access for Mallory Tested

Mallory's admin rights were tested by editing a protected file

Commands used:

```bash
su - mallory
sudo nano /etc/hosts
```

<img width="834" height="456" alt="image" src="https://github.com/user-attachments/assets/5e2f46d9-ee89-4f6b-952f-6998a68e40c2" />

---

## 10. Folder Clean-Up performed

The shared directory and all files inside were removed.

Command used:

```bash
sudo rm -r /home/shared
```

Verification 

```bash
ls /home
```

The shared directory is removed.

<img width="744" height="82" alt="image" src="https://github.com/user-attachments/assets/5ad8836e-512c-4ff2-aa01-c3369ffd7948" />

---

# Reflection

This exercise helped me understand how Linux manages users, groups and file permissions. I learned how to create users and groups, assign ownership, configure permissions using `chmod`, `chown` and `chgrp`, and verify access for different users. I also learned how administrator privileges using `sudo` can override normal permission restrictions.
