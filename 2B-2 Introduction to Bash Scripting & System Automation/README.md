# 2B-2 Introduction to Bash Scripting & System Automation

## Overview

Develop foundational skills in Bash scripting by learning file system operations, writing and executing scripts, using loops and conditionals, and automating system monitoring tasks.

# Deliverables

## 1. Directory and File Operations Completed

Created Directories, created and modified files, copied files, renamed file and removed files.

### Commands Used

```bash
mkdir LabFiles
cd Labfiles

touch notes.txt
echo "This is my first bash script." > notes.txt

cat notes.txt

cp notes.txt notes_backup.txt

mv notes_backup.txt backup_notes.txt

rm backup_notes.txt

ls -la
```

<img width="1005" height="237" alt="image" src="https://github.com/user-attachments/assets/2ffae362-cfc6-416e-8208-6ee583245bf1" />

---

## 2. Reflection : File System Commands

### What command did you use to create a directory?

I used 'mkdir' which makes a new directory.

### How can you view file content without using a GUI editor?

'cat' can be used to display file contents in the terminal

### What is the difference between 'cp' and 'mv'?

'cp' copies a file while keeping the original while 'mv' moves a file from one location to another

---

## 3. Basic bash Script Created and Run

A simple bash script was created to display a message.

### hello_world.sh

```bash
#!/bin/bash

echo "Hello World!"
```
### Commands used

```bash
chmod 777 hello_world.sh

./hello_world.sh
```

### Output

<img width="1089" height="323" alt="image" src="https://github.com/user-attachments/assets/91554c9a-a4be-401a-be00-5378b8f6eb62" />

<img width="462" height="85" alt="image" src="https://github.com/user-attachments/assets/49600015-8eee-4163-b99a-1584e4e26aab" />

---

## 4. Reflection: Script Basics

### What is `chmod +x` used for?

It gives permissions to run a a script as a program

### Why is `#!/bin/bash` used?

It tells Linux that the script should be interpreted using a Bash shell.

### How can you personalise script output?

Modify the text inside the 'echo' statement

---

## 5. Loop and Conditional Script

Created a Bash script to display user, loop, and validate user input.

### system_info.sh

```bash
#!/bin/bash

echo "Current User:"
whoami

echo ""

echo "Loop Example"

for i in {1..5}
do
    echo "Iteration $i"
done

echo ""

read -p "Enter a number: " number

if [ "$number" -lt 5 ]; then
    echo "The number is less than 5."

elif [ "$number" -le 10 ]; then
    echo "The number is between 5 and 10."

else
    echo "The number is greater than 10."

fi
```

### Commands used

```bash
chmod 777 system_info.sh

./system_info.sh
```

<img width="1083" height="613" alt="image" src="https://github.com/user-attachments/assets/04a7effa-0724-4ed3-8f09-20d376e27749" />

<img width="844" height="37" alt="image" src="https://github.com/user-attachments/assets/b99aa3ad-c8d2-4399-95c8-3fdc656f2c03" />

<img width="696" height="272" alt="image" src="https://github.com/user-attachments/assets/e144b89d-b07e-4a1e-ac55-fe2c95757ea7" />

<img width="593" height="222" alt="image" src="https://github.com/user-attachments/assets/94881a1c-7281-4b81-bd1b-f2ac511e657c" />

---

## 6. Reflection: Loops and Conditionals

### How does the 'for' loop work?

'for' loop repeats a command for each value in the specified range

### What Happens if the number is greater than 10?

the 'else' block is executed and displays that the number is greater than 10

### How could invalid input be handled more gracefully?

Ensure only numeric values are accepted before performing comparisons.

---

### 7. System Monitoring Script Created and Run

A Bash script was created to automate basic system monitoring tasks.

### resource_monitor.sh

```bash
#!/bin/bash

echo "===== CPU Usage ====="

top -b -n 1 | head -10

echo ""

echo "===== Memory Usage ====="

free -h

echo ""

echo "===== Disk Usage ====="

df -h
```


### Commands Used

```bash
chmod 777 resource_monitor.sh

./resource_monitor.sh
```

<img width="1077" height="551" alt="image" src="https://github.com/user-attachments/assets/ee17c134-d38f-466f-a2b1-e28ca9ab0066" />

<img width="1058" height="948" alt="image" src="https://github.com/user-attachments/assets/afdef1a5-f72c-48ca-80b8-864775ef659e" />

---

## 8. Reflection: Monitoring Automation

### What does 'free -h' show

It displays system memory usage

### How can this script be modified to monitor network usage?

The 'ip a' command can be added to the script to display network usage.

### Why is automation important for system administrators?

Automation reduces manual work, more consistent and saves time.

---

# Reflection

This activity introduced the basic concepts of Bash scripting and Linux automation. I learnt how to manipulate files using Linux commands, create executable Bash scripts, use loops and conditional statements to control program flow, and automate routine system monitoring tasks. These scripting techniques improve efficiency and provide a foundation for more advanced Linux system administration and automation.



