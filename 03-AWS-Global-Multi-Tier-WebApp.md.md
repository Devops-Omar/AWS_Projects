
![(103) Pro](https://github.com/user-attachments/assets/7fa6861c-a7f6-470a-9c31-b9f26a293f91)

# AWS Global Multi-Tier Web Application

This project demonstrates the deployment of a multi-tier web application infrastructure in AWS. It includes a VPC, subnets in different availability zones, EC2 instances, and configuration for global access and performance.

## Project Overview

The setup includes:
- **VPC** with CIDR block `10.0.0.0/16`.
- **Public and Private Subnets** across two availability zones (AZs).
- **EC2 Instances** for web and application layers in public subnets.
- **Domain Registration** with AWS Route 53.
- **Global Performance Optimization** using Amazon CloudFront and Route 53 for global user access.

## Requirements

- **Multi-Tier Architecture**:
  - Separate public and private subnets for different application tiers.
- **Domain Name Registration**:
  - Domain registered with AWS Route 53 for DNS management.
- **Global User Performance**:
  - Amazon CloudFront used as a Content Delivery Network (CDN) to improve access speed for users worldwide.
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

