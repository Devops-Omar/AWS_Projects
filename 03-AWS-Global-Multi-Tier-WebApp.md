![(103) Pro](https://github.com/user-attachments/assets/1fcfbc1a-be03-4d73-b448-aeea9a0db687)

# AWS Global Multi-Tier Web Application

This project demonstrates the deployment of a multi-tier web application infrastructure in AWS. It includes a VPC, subnets in different availability zones, EC2 instances, and configuration for global access and performance.

## Project Overview

The setup includes:
- **VPC** with CIDR block `10.0.0.0/16`.
- **Public and Private Subnets** across two availability zones (AZs).
- **EC2 Instances** for web and application layers in public subnets.
- **Domain Registration** with AWS Route 53.
- **Global Performance Optimization** using Amazon CloudFront and Route 53 for global user access.

- ## Key Features

- **Multi-Tier Architecture**:
  - Separate public and private subnets for different application tiers.
- **Domain Name Registration**:
  - Domain registered with AWS Route 53 for DNS management.
- **Global User Performance**:
  - Amazon CloudFront used as a Content Delivery Network (CDN) to improve access speed for users worldwide.
  - 
- **Security**:
  - Access control and security measures at Layer 4 for subnet and instance protection.

## Setup Instructions

1. **Create a VPC** with the specified CIDR block.
2. **Configure Subnets** in two availability zones:
   - Public subnets for web tier.
   - Private subnets for application tier.
3. **Deploy EC2 Instances** in public subnets for the application and web layers.
4. **Register the Domain** with Route 53 and set up DNS records.
5. **Optimize Global Performance** using CloudFront for better content delivery.

# Project Requirements

1. **VPC Setup**:
   - CIDR block `10.0.0.0/16`.
   - Public subnets: `10.0.10.0/24` (AZ A) and `10.0.20.0/24` (AZ B).
   - Private subnets: `10.0.100.0/24` (AZ A) and `10.0.200.0/24` (AZ B).

2. **Security**:
   - Layer 4 access control to secure both subnets and instances.

3. **EC2 Instances**:
   - Two EBS-backed EC2 instances in public subnets.

4. **Domain Name**:
   - Registered with AWS Route 53 for DNS management.

5. **Global Performance**:
   - Ensure good performance for users across the globe using Amazon CloudFront.

6. **Internet Gateway**:
   - Required for public subnets to connect to the internet.
  


