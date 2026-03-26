# Traditional 3-Tier WordPress Deployment on AWS

<p align="center">
  <img src="https://i.gyazo.com/397a121d21cbda916ec27dc874a03669.png" alt="Diagram" width="700">
  <br>
  <sub>Figure 1: Architecture Diagram</sub>
</p>

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

<p align="center">
  <img src="https://i.gyazo.com/84187e83823f8be44329111c0ec1abf4.png" alt="Subnets" width="700">
  <img src="https://i.gyazo.com/be61a7e413d09999a50034e8cb3be454.png" alt="EC2 Instance" width="500">
  <img src="https://i.gyazo.com/e5c8ea0d88294b77d9913fa642c0c8d2.png" alt="WordPress Install" width="700">
  <img src="https://i.gyazo.com/da56a31788e20cc8e0e28d100ce7a121.png" alt="ALB DNS" width="700">
  <br>
  <sub>Figure 2: Workflow</sub>
</p>

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

<p align="center">
  <img src="https://i.gyazo.com/846be14d863ddd65c3adc1f5d8ed5458.png" alt="Application" width="700">
  <br>
  <sub>Figure 3: Application</sub>
</p>

## Future Improvements
- Implement auto-scaling for EC2 instances  
- Configure backups and monitoring for RDS  
- Harden security and apply AWS WAF for web protection  
