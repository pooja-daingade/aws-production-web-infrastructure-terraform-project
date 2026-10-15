# AWS Production-Ready Web Infrastructure using Terraform

##  Project Overview

This project demonstrates the implementation of production-ready web infrastructure on Amazon Web Services (AWS) using Terraform.

The infrastructure is designed to provide scalability, secure networking, HTTPS access, and automated management of EC2 instances using Infrastructure as Code (IaC).

##  Project Objectives

- Automate AWS infrastructure provisioning using Terraform.
- Create a VPC with public and private subnets across multiple Availability Zones.
- Configure Internet Gateway and NAT Gateways.
- Deploy EC2 instances using a Launch Template and Auto Scaling Group.
- Distribute incoming traffic using an Application Load Balancer.
- Configure HTTPS using AWS Certificate Manager (ACM).
- Connect a custom domain using Amazon Route 53.
- Store Terraform state remotely in Amazon S3.

##  Project Architecture

The following architecture represents the AWS infrastructure implemented using Terraform.

<img width="1536" height="1024" alt="Architecture" src="https://github.com/user-attachments/assets/e5ad0586-f1b7-4c47-a205-a1e6ea715250" />


### Architecture Flow

Route 53 → Application Load Balancer → Target Group → EC2 Instances

The Auto Scaling Group manages EC2 instances using the Launch Template.

### Architecture Components

1. **Amazon VPC** – Provides an isolated network environment.
2. **Public and Private Subnets** – Organize resources across multiple Availability Zones.
3. **Internet Gateway (IGW)** – Provides internet connectivity to public resources.
4. **NAT Gateways** – Allow resources in private subnets to access the internet outbound.
5. **Security Groups** – Control inbound and outbound traffic.
6. **Amazon EC2** – Hosts the web server.
7. **Launch Template** – Defines the EC2 instance configuration.
8. **Auto Scaling Group (ASG)** – Manages EC2 instances automatically.
9. **Application Load Balancer (ALB)** – Distributes incoming web traffic across instances.
10. **Target Group** – Registers EC2 instances for load balancing.
11. **AWS Certificate Manager (ACM)** – Provides the SSL/TLS certificate for HTTPS.
12. **Amazon Route 53** – Routes domain traffic to the Application Load Balancer.
13. **Amazon S3** – Stores Terraform remote state.

##  Technologies Used

- Amazon Web Services (AWS)
- Terraform
- Amazon VPC
- Public and Private Subnets
- Internet Gateway
- NAT Gateway
- Security Groups
- Amazon EC2
- Launch Template
- Auto Scaling Group
- Application Load Balancer
- Target Group
- AWS Certificate Manager (ACM)
- Amazon Route 53
- Amazon S3

##  Implementation Steps

### 1. Networking

- Created a VPC with CIDR `10.0.0.0/16`.
- Created public and private subnets across three Availability Zones.
- Configured Internet Gateway and NAT Gateways.
- Configured route tables and Security Groups.

### 2. EC2 Configuration

- Created a Launch Template to define the EC2 instance configuration.
- Configured an Auto Scaling Group to manage EC2 instances.

### 3. Load Balancing

- Created a Target Group for EC2 instances.
- Configured an Application Load Balancer to distribute incoming web traffic.

### 4. HTTPS Configuration

- Configured an SSL/TLS certificate using AWS Certificate Manager.
- Enabled secure HTTPS access through the Application Load Balancer.

### 5. Domain Configuration

- Configured an Amazon Route 53 alias record.
- Connected the custom domain to the Application Load Balancer.

### 6. Terraform State Management

- Configured Amazon S3 as the remote backend for Terraform state storage.

##  Website Testing

**Domain:** https://prod-dev.poojadaingade.shop

The website was accessed through the custom domain to verify HTTPS connectivity.

Refreshing the webpage displayed different EC2 instance IDs, demonstrating traffic distribution between instances through the Application Load Balancer.

##  Project Documentation

Detailed project documentation, including implementation screenshots and configuration details, is available below.

[AWS-Production-Ready-Web-Infrastructure-Documentation.pdf](https://github.com/user-attachments/files/33476040/AWS-Production-Ready-Web-Infrastructure-Documentation.pdf)


##  Key Learnings

- Infrastructure as Code (IaC) using Terraform.
- AWS networking and subnet design.
- EC2 provisioning and automated instance management.
- Load balancing and traffic distribution.
- HTTPS configuration using ACM.
- DNS configuration using Route 53.
- Terraform remote state management using Amazon S3.

##  Conclusion

Successfully implemented a production-ready web infrastructure on AWS using Terraform.

This project provided hands-on experience with AWS networking, compute services, load balancing, Auto Scaling, HTTPS configuration, DNS management, and Infrastructure as Code.

##  Author

**Pooja Daingade**
