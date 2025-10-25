# AWS VPC + EC2 Web Server Lab

## Overview
This hands-on lab demonstrates how to design and deploy a **secure AWS Virtual Private Cloud (VPC)** with public and private subnets, EC2 instances, and a web server.  
It’s perfect for learning **AWS networking fundamentals** and showcasing your **cloud architecture skills**.

---

## What You Will Build
- A custom **VPC** with CIDR block (e.g., `10.0.0.0/16`)
- **2 Public Subnets** and **2 Private Subnets** across different Availability Zones
- **Internet Gateway (IGW)** for public access  
- **NAT Gateway** for private instances to reach the internet
- **EC2 Instances**
  - **Public EC2:** acts as a bastion host or web server  
  - **Private EC2:** internal server accessible only through the public instance
- **Security Groups** and **Route Tables** properly configured
- A **web server (Apache or Nginx)** running on the public EC2 instance

---

## Prerequisites
- AWS Free Tier account  
- Basic understanding of EC2 and networking  
- SSH key pair (`.pem` file)  
- *(Optional)* AWS CLI installed locally

---

## Steps (High-Level)

### 1. Create the VPC
- CIDR: `10.0.0.0/16`

### 2. Add Subnets
- Two **public**, two **private** (in different AZs)

### 3. Attach Internet Gateway  
- Enable internet access for public subnets

### 4. Configure Route Tables  
- Public subnets route → IGW  
- Private subnets route → NAT Gateway

### 5. Launch EC2 Instances  
- **Public EC2:** assign public IP  
- **Private EC2:** no public IP  

### 6. SSH into EC2
- From your laptop → connect to **Public EC2**  
- From **Public EC2** → connect to **Private EC2**

### 7. Install a Web Server
```bash
sudo yum update -y
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
echo "Hello from AWS Web Server!" | sudo tee /var/www/html/index.html

http://<your-public-ec2-public-ip>


# 🧠 AWS VPC + EC2 Web Server Lab

## 🌍 Overview
This hands-on lab demonstrates how to design and deploy a **secure AWS Virtual Private Cloud (VPC)** with public and private subnets, EC2 instances, and a web server.  
It’s perfect for learning **AWS networking fundamentals** and showcasing your **cloud architecture skills**.


## What You Will Build
- A custom **VPC** with CIDR block (e.g., `10.0.0.0/16`)
- **2 Public Subnets** and **2 Private Subnets** across different Availability Zones
- **Internet Gateway (IGW)** for public access  
- **NAT Gateway** for private instances to reach the internet
- **EC2 Instances**
  - **Public EC2:** acts as a bastion host or web server  
  - **Private EC2:** internal server accessible only through the public instance
- **Security Groups** and **Route Tables** properly configured
- A **web server (Apache or Nginx)** running on the public EC2 instance


## Prerequisites
- AWS Free Tier account  
- Basic understanding of EC2 and networking  
- SSH key pair (`.pem` file)  
- *(Optional)* AWS CLI installed locally

---

## 🪜 Steps (High-Level)

### 1. Create the VPC
- CIDR: `10.0.0.0/16`

### 2. Add Subnets
- Two **public**, two **private** (in different AZs)

### 3. Attach Internet Gateway  
- Enable internet access for public subnets

### 4. Configure Route Tables  
- Public subnets route → IGW  
- Private subnets route → NAT Gateway

### 5. Launch EC2 Instances  
- **Public EC2:** assign public IP  
- **Private EC2:** no public IP  

### 6. SSH into EC2
- From your laptop → connect to **Public EC2**  
- From **Public EC2** → connect to **Private EC2**

### 7. Install a Web Server
```bash
sudo yum update -y
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
echo "Hello from AWS Web Server!" | sudo tee /var/www/html/index.html
````

### 8. Test in Browser

Visit:

```
http://<your-public-ec2-public-ip>
```

---

## 🎯 Learning Objectives

* Understand how AWS VPC networking works
* Learn how to route traffic between public/private subnets
* Practice using EC2, Security Groups, and Route Tables
* Build a **portfolio-ready AWS architecture**

---

## Author

**Babajide Amure**
AWS Instructor | Cloud & DevOps Consultant
📍 Abuja, Nigeria
🌐 [jaydeploy.com](https://www.jaydeploy.com)

