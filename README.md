**AWS VPC + EC2 Web Server Lab**

**Overview**
This hands-on lab demonstrates how to design and deploy a secure AWS Virtual Private Cloud (VPC) with public and private subnets, EC2 instances, and a web server.
It’s perfect for learning AWS networking fundamentals and showcasing cloud architecture skills.

**What You will Build**
A custom VPC with CIDR block (e.g., 10.0.0.0/16)
2 Public Subnets and 2 Private Subnets across different Availability Zones
Internet Gateway (IGW) for public access
NAT Gateway for private instances to reach the internet
EC2 Instances
Public EC2: acts as a bastion host or web server
Private EC2: internal server accessible only through the public instance
Security Groups and Route Tables properly configured
A web server (Apache or Nginx) running on the public EC2

**Prerequisites**
AWS Free Tier account
Basic understanding of EC2 and networking
SSH key pair (.pem file)
Optional: AWS CLI installed locally

**Steps (High-Level)**
Create the VPC
Use CIDR 10.0.0.0/16
Add Subnets
Two public, two private (in different AZs)
Attach Internet Gateway
Configure Route Tables
Launch EC2 Instances
Public EC2 → assign public IP
Private EC2 → no public IP
SSH into EC2
Connect to the public EC2 from your laptop
Then SSH into private EC2 from the public EC2

**Install a Web Server**
sudo yum update -y
sudo yum install -y httpd
sudo systemctl start httpd
sudo systemctl enable httpd
echo "Hello from AWS Web Server!" | sudo tee /var/www/html/index.html


**Test in Browser**
Visit http://<public-ec2-public-ip>

**Learning Objectives**
Understand how AWS VPC networking works
Learn how to route traffic between public/private subnets
Practice using EC2, security groups, and routing
Build a portfolio-ready AWS architecture

**Author**
Babajide Amure
AWS Instructor | Cloud & DevOps Consultant
Abuja, Nigeria
jaydeploy.com
