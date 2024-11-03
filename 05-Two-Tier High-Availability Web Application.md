![4](https://github.com/user-attachments/assets/f527dff5-4b39-4ee4-b797-9f23e6f77163)

# AWS Two-Tier High-Availability Web Application

This project demonstrates the deployment of a highly available, two-tier web application infrastructure in AWS. The setup includes VPCs, public and private subnets, an internet-facing ELB, EC2 instances for web/app tiers, and RDS for the database tier.

## Project Overview

The setup includes:
- **VPC** with public and private subnets across two availability zones for high availability.
- **Web/App Tier**: EC2 instances in private subnets, with inbound traffic permitted only from the ELB.
- **Database Tier**: RDS instances in private subnets that are inaccessible from the internet.
- **Security**: SSL offloading on the ELB, secure communication, and appropriate security group rules.
# Project Requirements

1. **Web/App and Database Tier Separation**:
   - Web/app and database tiers must be in separate subnets and cannot share routing tables.
   - Must not be directly accessible from the internet.

2. **High Availability**:
   - Infrastructure should be deployed in multiple availability zones.

3. **Subnets**:
   - Minimum required subnets for design:
     - Public subnets for load balancer nodes.
     - Private subnets for web/app EC2 instances.
     - Private subnets for RDS database instances.

4. **Internet-Facing ELB**:
   - Distribute incoming traffic to the web/app tier.
   - Inbound traffic to web/app EC2 instances must be permitted only from the ELB.

5. **SSL Offloading**:
   - Protect client-to-application traffic with SSL (offloaded to the ELB).

6. **Database Security**:
   - RDS instances should be accessible only from web/app tier and not from the internet.

- ## Setup Instructions

1. **VPC and Subnets**:
   - Create a VPC with subnets in two availability zones.
   - Set up public subnets for ELB and private subnets for EC2 and RDS instances.
2. **Load Balancer**:
   - Configure an internet-facing ELB with SSL offloading.
3. **EC2 and RDS Instances**:
   - Launch web/app tier EC2 instances in private subnets.
   - Deploy RDS instances for the database tier with multi-AZ support.
4. **Security Configuration**:
   - Configure security groups to ensure only ELB can access the EC2 instances.
   - Implement SSL offloading on the ELB.
