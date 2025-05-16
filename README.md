# AWS 3-Tier Web Application Architecture using Terraform

This project builds a highly available and scalable 3-tier web application infrastructure on AWS using Terraform. It includes a public-facing Application Load Balancer, an Auto Scaling group of EC2 instances for the application layer, and an RDS MySQL database for persistent storage.

## 📌 Project Overview

This architecture is designed for production-ready, fault-tolerant, and secure deployments across multiple availability zones.

# Architecture

<img width="663" alt="Screenshot 2025-05-17 at 1 47 24 AM" src="https://github.com/user-attachments/assets/e0bbdf83-a5ce-4d5e-bb55-fe9e357c4b76" />



### Architecture Summary

- **VPC** with 6 subnets across 2 AZs:
  - 2 Public Subnets (for ALB)
  - 2 Private Subnets (for EC2 app layer)
  - 2 Private Subnets (for RDS database layer)
- **Internet Gateway** for public access
- **NAT Gateways** (1 per AZ) for secure internet access from private subnets
- **Application Load Balancer (ALB)** for distributing traffic across EC2 instances
- **Auto Scaling Group (ASG)** with Launch Template for application EC2 instances
- **RDS MySQL Instance** (DB Instance with Read Replica )
- **Security Groups** for granular traffic control

---

## 🛠️ Tools & Technologies

- **AWS** (EC2, VPC, Subnets, ALB, RDS, NAT, IGW, Security Groups, etc.)
- **Terraform** (Infrastructure as Code)
- **Amazon-Linux** AMI for EC2 instances

