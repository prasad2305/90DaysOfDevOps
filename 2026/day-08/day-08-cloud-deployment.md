# Cloud Server Setup: Docker, Nginx & Web Deployment

## Task

Today’s goal is to deploy a real web server on the cloud and learn practical server management.

You will:
- Launch a cloud instance (AWS EC2 or Utho)
- Connect to the instance via SSH
- Install Nginx web server
- Configure security groups (open port 80 for HTTP access)
- Extract and save Nginx logs
- Verify the web page is accessible from the browser

---

# Launch Cloud Instance (AWS EC2)

### Step 1 : Action
- Go to AWS EC2 Console
- Click **Launch Instance**

### Choose:
- AMI: Ubuntu / Amazon Linux
- Instance type: t2.micro (free tier)
- Key pair: Create or use existing key



### Step 2: Connect via SSH

`ssh -i "C:\Users\prsds\Downloads\devops.pem" ec2-user@54.163.16.241`


# Install Nginx 

### Step 3: Update System Packages

`sudo yum update -y`

### Step 4: Install Nginx

`sudo yum install nginx -y`

### Step 5: Start Nginx Service

`sudo systemctl start nginx`

`sudo systemctl enable nginx`

`sudo systemctl status nginx`

### Step 6: Verify Nginx Service is Running
`sudo systemctl status nginx`

# Security Group Configuration 
Ensure inbound rule:

HTTP (80) -  0.0.0.0/0
### Step 7: Open Browser and Test Web Server
`http://<public-ip>`
http://54.163.16.241/

Expected Result:

Nginx Welcome Page should be visible

# Docker on Linux (Amazon Linux / EC2)

### Step 8: Update System Packages
`sudo yum update -y`

### Step 9: Install Docker
`sudo yum install docker -y`

### Step 10: Start Docker Service
`sudo systemctl start docker`

### Step 11: Enable Docker (auto start on reboot)
`sudo systemctl enable docker`

### Step 12: Check Docker Status
`sudo systemctl status docker`

### Step 13: Verify Docker Installation
`docker --version`

### Step 14 : Check Docker service (system logs)

This shows logs of the Docker daemon (engine)

`sudo journalctl -u docker -f`


# Extract Nginx Logs

### Step 15: Check Nginx Logs 
`sudo cat /var/log/nginx/access.log`

`sudo cat /var/log/nginx/error.log`


### Step 16: Download Log File to Local Machine
Run this on your local system (not EC2):
`scp -i "C:\Users\prsds\Downloads\devops.pem" ec2-user@54.163.16.241:/var/log/nginx/access.log .`
