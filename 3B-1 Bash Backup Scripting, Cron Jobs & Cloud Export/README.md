# Bash Backup Scripting, Cron Jobs & Cloud Export

## Overview

Write a Bash script that creates a dated ZIP backup of the /home/ubuntu/Documents directory every hour using cron, and optionally exports it to a remote cloud server using scp. 

---

# Deliverables

## 1. Practice Bash Commands Executed

Bash commands were used to familiarise with shell scripting.

### Commands used

```bash
echo "Hello World"

name="Cornelius"
echo $name

num1=10
num2=20
echo $((num1 + num2))

sum=0

for i in {1..10}
do
    sum=$((sum+i))
done

echo $sum
```

<img width="721" height="366" alt="image" src="https://github.com/user-attachments/assets/9de26ee7-67a1-48e7-9514-c54da8edfa0c" />

---

## 2. Test Files & Directories Created 

Files were created inside the documents folder.

### Commands used

```bash
mkdir -p ~/Documents/LabFiles

touch ~/Documents/LabFiles/file1.txt
touch ~/Documents/LabFiles/file2.txt
touch ~/Documents/LabFiles/file3.txt

mkdir ~/Documents/Reports

touch ~/Documents/Reports/report1.txt
```

<img width="604" height="351" alt="image" src="https://github.com/user-attachments/assets/04d7473b-355f-47c9-9487-862defc6c52c" />

---

## 3. Basic Script Working

Bash script named 'testscript' was create and tested.

Bash script created

<img width="1076" height="714" alt="image" src="https://github.com/user-attachments/assets/c672d1c8-68f5-49d6-ac62-1f029adbc665" />

### Script Features

- Created a backup folder
- Copies all files recursively
- Displays completion message

Commands used:

```bash
mkdir -p /home/ubuntu/backup

cp -r /home/ubuntu/Documents/* /home/ubuntu/backup/

sudo chmod 777 testscript
```

<img width="678" height="309" alt="image" src="https://github.com/user-attachments/assets/f433456f-d250-43da-a702-4f5afd479342" />

---

## 4. Script Installed as System Command

Output shows:

- Script moved to /usr/bin/testscript 
- sudo chown applied 
- Testscript works from any directory

### Commands used

```bash
sudo mv testscript /usr/bin/

sudo chown root:root /usr/bin/testscript

sudo chmod 755 /usr/bin/testscript
```

<img width="1047" height="407" alt="image" src="https://github.com/user-attachments/assets/e3a35451-6f5e-4b6e-8476-3ebf97e4fe19" />

---

## 5. ZIP Archive with Date Filename

The script was updated to compress the backup folder into a ZIP file.

Command used:

```bash
now=$(date +"%d_%m_%y")

zip -r /home/ubuntu/$now.zip /home/ubuntu/backup
```

<img width="783" height="199" alt="image" src="https://github.com/user-attachments/assets/bdbe9854-b54d-4dd4-8692-fdda882b71cb" />

<img width="685" height="14" alt="image" src="https://github.com/user-attachments/assets/b69c3a00-1e61-42bb-a40f-176ab54b9c90" />

---

## 6. Cronjob Set Up for Daily Backup

The backup script was scheduled to run automatically everyday.

Cron entry:

```cron
9 * * * *  ubuntu /usr/bin/testscript
```

<img width="1073" height="536" alt="image" src="https://github.com/user-attachments/assets/cbadef0a-7aca-48d4-9477-ce6770b60ac0" />

---

## 7. Successful Cron Execution Verified

Cron successfully execueted the script.

<img width="652" height="65" alt="image" src="https://github.com/user-attachments/assets/816a9c9a-7486-4d3c-b083-459ab3d24b54" />

---

## 8. SCP to Cloud Working

SCP was used to transfer the backup archive to another Linux server.

Command used:

```bash
scp -i /home/ubuntu/aws-ubuntu-key.pem \
/home/ubuntu/$now.zip \
ubuntu@13.229.243.48/home/ubuntu/
```

<img width="2358" height="1328" alt="image" src="https://github.com/user-attachments/assets/46f8d05b-5eff-4dda-9b86-6a7c57b5c9f1" />

---

## 9. SSH Certificate Accepted by Root

SSH key fingerprint was accepted

<img width="2358" height="1328" alt="image" src="https://github.com/user-attachments/assets/eda524a9-eeb2-4bad-86fb-2a8c8d739442" />

---

## 10. Final Script Submitted

The completed backup script performs the following tasks:

<img width="816" height="375" alt="image" src="https://github.com/user-attachments/assets/bba09e77-1e83-458d-b971-3cfff5a69f8f" />

---

# Reflection

This activity demonstrated how Bash scripting can automate repetitive system administration tasks. I learnt how to use variables, loops, and arithmetic operations within shell scripts, automate file backups, compress files into ZIP archives, schedule tasks using Cron, and securely transfer files between Linux servers using SCP. These techniques improve efficiency, reduce manual effort, and form the foundation of automated backup solutions commonly used in Linux system administration.



