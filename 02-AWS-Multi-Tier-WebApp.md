# AWS Multi-Tier Web Application Setup

This project demonstrates the setup of a multi-tier web application infrastructure in AWS. It includes the creation of a VPC, public and private subnets, EC2 instances, security configurations, and access control for developers and administrators.

## Project Overview

The setup includes:
- **VPC** with a CIDR block of `10.0.0.0/16`.
- **2 Public Subnets**:
  - `10.0.10.0/24` in Availability Zone A.
  - `10.0.20.0/24` in Availability Zone B.
- **2 Private Subnets**:
  - `10.0.100.0/24` in Availability Zone A.
  - `10.0.200.0/24` in Availability Zone B.
- **EC2 Instances**:
  - Two EBS-backed EC2 instances, one in each public subnet, acting as the web and application tiers.
- **Security and Access Control**:
  - Detailed security measures at Layer 4 for subnet and instance-level protection.
  - Programmatic access configuration for developers and administrators.

## Requirements

## Setup Instructions

1. **VPC Creation**: Set up a VPC with the CIDR block `10.0.0.0/16`.
2. **Subnets Configuration**: Create public and private subnets in two different AZs.
3. **Internet Gateway**: Attach an Internet Gateway for public subnet access.
4. **EC2 Instances**: Launch EBS-backed EC2 instances in the public subnets.
5. **Security**: Implement security groups and access control lists for Layer 4 protection.


![(102)](https://github.com/user-attachments/assets/e7e4d307-0223-443c-90e7-c9443570c628)
