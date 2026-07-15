# 2B-1 Cloud Web Server Deployment with Amazon EC2

## Overview

Launch a cloud-based Linux virtual machine using AWS EC2 (or other cloud platforms), install Apache, serve web pages and downloadable files, and learn basic hosting concepts. 

---

# Deliverables

## 1. EC2 Instance Launched

I ran a Ubuntu EC2 instance using AWS

<img width="798" height="34" alt="image" src="https://github.com/user-attachments/assets/7fc0f84d-6345-4204-b4a1-79de0fa87887" />
<img width="591" height="26" alt="image" src="https://github.com/user-attachments/assets/65d9f887-5db5-45b6-879a-ebdf93a2fd9b" />
<img width="183" height="54" alt="image" src="https://github.com/user-attachments/assets/816b7a1d-63be-4670-8edd-4ed1916bbce9" />
<img width="818" height="693" alt="image" src="https://github.com/user-attachments/assets/d35afb14-6c3c-4940-891d-14c61939dcc1" />

---

## 2. Security Group Configured

The EC2 Security was configured with Port 22 and 80 opened

<img width="783" height="255" alt="image" src="https://github.com/user-attachments/assets/05155309-7b8c-45d3-8993-6abe889bedbd" />

---

## 3. SSH Access Successful

A SSH login was established using .pem key

### Command used

```bash
ssh -i ~/Downloads/aws-ubuntu-key.pem ubuntu@54.169.64.255
```

<img width="994" height="558" alt="image" src="https://github.com/user-attachments/assets/d6150b98-3650-4764-bc56-91d04e45c6ec" />

---

## 4. Apache Installed and Tested

Apache2 was installed in the earlier labs.

http://172.17.0.1

---

## 5. Custom index.html Edited

The default webpage was personalized.

### Command Used

```bash
sudo nano/var/www/html/index.html
```

<img width="1014" height="246" alt="image" src="https://github.com/user-attachments/assets/0c3511cf-c6cc-4a06-b27c-0a3fa807b2e1" />

<img width="1030" height="242" alt="image" src="https://github.com/user-attachments/assets/1fdad263-a98c-436e-b942-32775a442afa" />

---

## 6. External File Downloaded with wget

Downloaded a PDF using wget

### Command Used

```bash
wget https://www.w3.org/WAI/ER/tests/xhtml/testfiles/resources/pdf/dummy.pdf
```

<img width="947" height="266" alt="image" src="https://github.com/user-attachments/assets/fe6e54e8-90c3-4741-bd33-366dde384250" />

---

## 7. File Copied to Web Root

The downloaded PDF was copied to Apache

### Command used

```bash
ls -l /var/www/html
```

<img width="654" height="106" alt="image" src="https://github.com/user-attachments/assets/22d76611-18a2-4afa-9e35-6ee60b6548a8" />

---

## 8. PDF File Accessible via Browser

The uploaded PDF was able to be accessed through the web browser.

<img width="1064" height="868" alt="image" src="https://github.com/user-attachments/assets/482e1e54-7987-4bff-9076-b933c999671f" />

---

## 9. Link Inserted in HTML Page

A hyper link was added to the PDF file

```html
<a href="dummy.pdf">Click here to download the PDF</a>
```

<img width="1181" height="359" alt="image" src="https://github.com/user-attachments/assets/a070387b-6364-4d0d-a1b4-073f1e91078d" />

---

## 10. Budget Monitoring Enabled

AWS Billing dashboard was configured.

<img width="788" height="497" alt="image" src="https://github.com/user-attachments/assets/6eae4a26-4917-4fb1-a720-24b7000a0876" />

---

# Reflection

This activity introduced the deployment of a web server using Amazon EC2. I learnt how to launch and manage cloud instances, configure security groups, establish secure SSH connections, install Apache, host web content, and provide downloadable files over HTTP. I also gained experience with AWS cost management by configuring budget monitoring and understanding the importance of stopping or terminating cloud resources when they are no longer needed.

