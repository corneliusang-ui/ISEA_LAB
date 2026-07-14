# 1B-3 File Extraction, Searching & Pattern Analysis (Gutenberg Archive)

## Overview

Learn to extract compressed archives and apply advanced command-line file search techniques (by filename, content, date, size) to solve real problems on a Linux filesystem. 

 ---

 # Deliverables

 ## 1. Archive Extracted Successfull

 The compressed Gutenberg archive was decompressed and extracted successfully.

 Commands used:

 ```bash
bunzip2 1b-3-Gutenberg.tar.bz2

tar -xvf 1b-3-Gutenberg.tar
```

The extracted files were successfully restored into the directory.

<img width="733" height="147" alt="image" src="https://github.com/user-attachments/assets/29f73fe7-cf42-4e8a-913b-2aa42940b465" />

---

## 2. File Listing of Extracted Directory

The extracted directoryy contents were verified using file listing commands.

Commands used:

```bash
ls -l
```

The ouput shows that all files were successfully extracted.

<img width="696" height="111" alt="image" src="https://github.com/user-attachments/assets/1cef5ce2-bab2-476f-b0a6-e87604719849" />

---

## 3. Filename Search Demonstrated

'find' was used to search for files based on their filename or similar extensions

Command used:

```bash
find . -name "*.txt"

```

The command displaed all text files within the current director and its sub directories

<img width="713" height="99" alt="image" src="https://github.com/user-attachments/assets/949b88f8-2efe-47bf-b50a-113837564734" />

---

## 4. Text Search via Grep

'grep" was used to search for the words in the txt files.

Command used:

```bash
grep -r "disaster" .
```

The matching files nad lines containing "disaster" were displayed.

<img width="997" height="69" alt="image" src="https://github.com/user-attachments/assets/5f8dd40c-881f-4ef3-8b09-91a2e44aaf77" />

---

## 5. Contextual Text Search

'grep' was used together with '-C' to display surrounding lines.

Command used:

```bash
grep -r -C 2"disaster" .
```

<img width="1027" height="69" alt="image" src="https://github.com/user-attachments/assets/4f3cc2b3-feba-4724-b051-4b96f88c22fe" />

---

## 6. Data-Based File Searches

File information was viewed using:

```bash
ls -lh
```

This displayed the file names, permissions and file sizes.

<img width="1053" height="107" alt="image" src="https://github.com/user-attachments/assets/cac249c5-ac0d-489b-8e59-99f3520e5345" />

---

## 7. Sized-Based File Searches

Files were searched based on size.

Command used: 

```bash
find . -type f -size +1c
```

<img width="741" height="205" alt="image" src="https://github.com/user-attachments/assets/3a4a42ba-5d56-4842-b85d-7b390ba9af27" />

---

## 8. Largest Files Found

Disk usage for the extracted files was shown.

Command used:

```bash
du -ah .
```

This showed the amount of disk space each file used.

<img width="632" height="103" alt="image" src="https://github.com/user-attachments/assets/ee259d5c-b4fb-4453-b695-e6e5d28c4f04" />

---

## 9. Text Frequency Analysis Performed

The contents of the text file were processed using 'sed'.

Command used:

```bash
sed 's/ /\n/g' frankenstein.txt
```

<img width="774" height="269" alt="image" src="https://github.com/user-attachments/assets/2441bedc-0805-4230-825e-118ed626adc2" />

## 10. Answers to Questions Provided

Deliverable not done because all questions has nothing to do with the given Guternberg zip folder.

# Reflection

This exercise helped me become more familiar with Linux file management and text-processing commands. I learned how to extract compressed archives, search for files using `find`, search file contents using `grep`, display file sizes with `du`, and manipulate text using `sed`. These tools are useful for locating information and managing files efficiently from the command line.





