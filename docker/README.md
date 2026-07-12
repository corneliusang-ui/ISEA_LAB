# Docker Service

## Overview

This folder contains the docker setup for the additional server service. I used an Ubuntu EC2 instance and deployed a Nginx container.

---

## Environment 

- Ubuntu server (AWS EC2)
- Docker Engine
- GitHub
- Nginx

---

## Steps

### 1. I Checked if Docker was installed.

```bash
docker --version
```

Example output:

```
Docker version 29.6.1
```

---

### 2. Downloading the Nginx Image

I downlaoded the Nginx image from the Docker hub.

```bash
docker pull nginx
```

---

### 3. Creating and Running the container

```bash
docker run -d --name my-nginx -p 80808:80 nginx
```

This command will start the container in the background and map port 8080 on the EC2 server to port 80 in the container

---

### 4. Check if the container is running

To make sure if the container is successfully running, I ran:

```bash
docker ps
```

The output showed that Nginx is working

---

### 5. Checking the port

Checking whether the Docker is conneceted to port 8080

```bash
sudo ss -tlnp | grep 8080
```

This confirmed that the container was on the correct port

---

### 6. Configuring the security group

To allow others to access the web server, I added an additional inbound rule to the AWS EC2 security group

| Custom TCP | TCP | 8080 | 0.0.0.0/0 |

---

### 7. Checking the firewall

I checked whether the Ubuntu firewall to make sure port 8080 is not blocked

```bash
sudo ufw status
```

To be safe, I also allowed the port using:

```bash
sudo ufw allow 8080/tcp
```

---

### 8. Testing the web server

I tested the web server on EC2 by running:

```bash 
curl http://localhost:8080
```

The command showed the NginX HTML page which shows that the web server is working.

---

### 9. Opening the website

Lastly, I opened the website using the EC2 public IP address.

```
http://54.169.64.25:8080
```

I was greeted by the Nginx welcome page in the browser which also confirmed that the container was running correctly.

## Screenshots

The screenshots folder contains:

- Docker installtion
- Docker version
- Downloading Nginx image
- Running the docker container
- Output of docker ps
- AWS Security Group settings
- Nginx page in browser

---

## What I learned

This assignment helped me to understand basic Docker workflow. I learned how to download an image, create a container, expose ports, and check that the container was running correctly.
 I also learned that the AWS Security Group and firewall settings are important because they can stop users from accessing the application even if the container is running.
