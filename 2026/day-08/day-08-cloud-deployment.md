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

`ssh -i "dovops.pem" ec2-user@ec2-54-175-61-228.compute-1.amazonaws.com`


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


# Extract Nginx Logs

### Step 14: Check Nginx Logs 
`sudo cat /var/log/nginx/access.log`

`sudo cat /var/log/nginx/error.log`

### Step 15: Save Logs to File
`sudo cat /var/log/nginx/access.log > nginx-logs.txt`

`sudo cat /var/log/nginx/error.log >> nginx-logs.txt`

### Step 16: Verify Log File
`cat nginx-logs.txt`

### Step 17: Download Log File to Local Machine
Run this on your local system (not EC2):
`scp -i "dovops.pem" ec2-user@ec2-54-175-61-228.compute-1.amazonaws.com:~/nginx-logs.txt .`
