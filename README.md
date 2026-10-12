### 📚 Library Management System on AWS 

# 📌 Project Overview 

The Library Management System on AWS is a web application hosted on Amazon EC2 using Nginx. The project demonstrates AWS cloud infrastructure concepts such as VPC networking, public and private subnets, internet-facing and internal Load Balancers, Auto Scaling Groups, AMIs, and Launch Templates.

The website provides a user-friendly interface for browsing books, registering library members, issuing and returning books, and submitting feedback.


# 🎯 Project Objectives 

Deploy a website on Amazon EC2 using Nginx.

Configure a Virtual Private Cloud (VPC) with public and private subnets.

Distribute incoming traffic using an internet-facing Application Load Balancer.

Configure an internal Load Balancer for private network traffic.

Use Auto Scaling Groups to maintain EC2 instance capacity.

Create AMIs and Launch Templates for consistent instance deployment.

Understand cloud networking, availability, scalability, and security.


# ☁️ AWS Services Used 

Service

Purpose

Amazon VPC

Provides an isolated virtual network

Public Subnets

Host resources that require public routing

Private Subnets

Isolate internal resources from direct internet access

Internet Gateway

Provides internet routing for eligible public resources

Route Tables

Control network traffic routing

Amazon EC2

Hosts the website

Nginx

Serves the website files

Application Load Balancer

Distributes incoming HTTP/HTTPS traffic

Internal Load Balancer

Routes traffic within the private network

Target Groups

Register targets and monitor their health

Auto Scaling Group

Maintains the configured number of EC2 instances

Amazon Machine Image (AMI)

Provides a reusable EC2 instance image

Launch Template

Defines EC2 instance launch configuration

Amazon CloudWatch

Supports monitoring and scaling policies when configured


# 💻 Technologies Used 

HTML5

CSS3

JavaScript

Nginx

Amazon Linux

AWS EC2

AWS VPC

Application Load Balancer

Auto Scaling

AMI and Launch Templates


# ✨ Application Features 

Home Page: Overview of the Library Management System.

Books Page: Displays the book catalogue with search and category filtering.

Members Page: Provides a member registration form.

Issue Book: Accepts member ID, book ID, and issue date.

Return Book: Accepts issue ID and return date.

Feedback Page: Provides a form for submitting feedback.

About Page: Displays project information and technologies.

The frontend is built using HTML, CSS, and JavaScript. The website is served by Nginx on Amazon EC2.


# Deployment Steps 

# 1. Create the VPC 

Create a VPC.

Configure public and private subnets.

Create and associate route tables.

Attach an Internet Gateway to the VPC.

Configure security groups according to the architecture.

# 2. Launch EC2 Instances 

Launch Amazon Linux EC2 instances.

Configure the required instance type and security groups.

Install Nginx on the instances.

Example commands:

sudo dnf update -y
sudo dnf install nginx -y
sudo systemctl enable --now nginx

# 3. Deploy the Website

Copy the website files into the Nginx document root:

/usr/share/nginx/html/

Verify that Nginx is running:

sudo systemctl status nginx

# 4. Configure the Load Balancers

Create a target group.

Configure the target group health check.

Create an internet-facing Application Load Balancer.

Register the appropriate EC2 targets.

Configure the listener.

Create an internal Load Balancer if required by the private-tier architecture.

# 5. Create an AMI and Launch Template

Create an AMI from a configured EC2 instance.

Create a Launch Template using the AMI.

Specify the instance type, security groups, and other required settings.

# 6. Configure Auto Scaling

Create an Auto Scaling Group using the Launch Template.

Select the required subnets.

Configure minimum, desired, and maximum capacity.

Attach the appropriate target group.

Configure health checks and scaling policies as needed.

# 🧪 Testing and Validation

The following tests can be used to validate the deployment:

# Test 1: Website Availability

Access the website using the Load Balancer DNS name.

Verify that the homepage and other pages load correctly.

# Test 2: Target Group Health

Open the target group in the AWS Console.

Verify that the registered EC2 instances are healthy.

# Test 3: Load Balancing

Send repeated requests through the Load Balancer.

Use instance-specific information, such as hostname or private IP, to verify which EC2 instance handled a request.

# Test 4: Auto Scaling

Terminate a test EC2 instance managed by the Auto Scaling Group.

Check the Auto Scaling activity history.

Verify that a replacement launches when the group is configured to maintain desired capacity.

# Test 5: Internal Load Balancer

Access the internal Load Balancer from an authorized resource in the private network.

Verify connectivity to its configured targets.

# Test 6: AMI and Launch Template

Launch a test instance using the Launch Template.

Verify the operating system, Nginx service, and website files.

# 📚 Learning Outcomes

This project provides practical experience with:

AWS VPC networking and subnet design.

EC2 provisioning and Nginx configuration.

Load Balancer and Target Group setup.

Auto Scaling and instance replacement.

AMI creation and Launch Template configuration.

Security groups and network traffic control.

Hosting and validating a web application in the cloud.

# 👨‍💻 Conclusion

The Library Management System on AWS demonstrates how a web application can be hosted using EC2 and Nginx while leveraging AWS networking, Load Balancers, Auto Scaling, AMIs, and Launch Templates. The project combines frontend development with practical cloud infrastructure deployment and management.
