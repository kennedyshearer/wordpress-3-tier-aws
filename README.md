# Traditional 3-Tier WordPress Deployment on AWS

![Architecture Diagram Placeholder](images/architecture-diagram.png)

## Overview
This project demonstrates a production-grade 3-tier WordPress deployment on AWS. It separates networking, compute, database, and load balancing layers to ensure scalability, reliability, and security. The architecture is suitable for high-traffic websites requiring enterprise-level availability.

## Problem Statement
Single-tier or unstructured deployments limit scalability, security, and fault tolerance. Manual configuration of networking, compute, and database layers increases the risk of errors. The challenge was to design a repeatable, secure, and highly available 3-tier architecture for WordPress.

## Solution
- VPC with public and private subnets  
- NAT Gateways for secure internet access for private resources  
- ALB distributes traffic across EC2 WordPress instances  
- RDS MySQL database in private subnets  
- Security Groups and IAM Roles enforce fine-grained access  
- Fully automated deployment and monitoring for production readiness  

![Workflow / Implementation Placeholder](images/workflow.png)

## Steps to be Performed 👩‍💻
1. Networking Setup: VPC, subnets, NAT Gateways  
2. Database Setup: RDS MySQL, EFS storage  
3. Compute Setup: EC2 instances, ALB, security groups  
4. Test and validate high availability  

## Key Services / Tools Used 🛠
- Amazon VPC [Networking]  
- Internet Gateway / NAT Gateway [Networking]  
- Application Load Balancer (ALB) [Load Balancing]  
- Amazon EC2 [Compute]  
- Amazon RDS [Database]  
- IAM Roles & Policies [Security]  
- Security Groups [Traffic Control]  

## Results
![Application Screenshot Placeholder](images/results.png)  

## Future Improvements
- Implement auto-scaling for EC2 instances  
- Configure backups and monitoring for RDS  
- Harden security and apply AWS WAF for web protection  
