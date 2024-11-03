![Basion-Host](https://github.com/user-attachments/assets/a26e82ff-b62c-4034-a35b-ec9d0a8b084e)


# AWS Two-Tier Web Application Setup

This project demonstrates the deployment of a highly-available, fault-tolerant, two-tier web application infrastructure in a single AWS region. The setup includes VPCs, subnets, bastion hosts, NAT gateways, and EC2 instances for the application and database tiers.

## Project Overview

The setup includes:
- **VPC** with a CIDR block of `10.0.0.0/16`.
- **Public and Private Subnets** in two availability zones (AZs) for high availability.
- **Bastion Hosts** in the public subnets for secure SSH access to private subnets.
- **NAT Gateways** for allowing the private subnets to access the internet for updates without direct exposure.
- **EC2 Instances** in private subnets for the database layer, secured from direct internet access.
- **Security Configuration** to restrict access to database instances only to the corporate data center.


# Project Requirements

1. **VPC and Subnets**:
   - CIDR block `10.0.0.0/16`.
   - Public subnets in two availability zones for application access.
   - Private subnets in the same availability zones for database servers.

2. **Database Security**:
   - Database servers should not be accessible from the internet.
   - They should be able to access the internet through a NAT gateway for updates.

3. **SSH Access**:
   - Database administrators must access the database instances via SSH.
   - Access should only be allowed from the corporate data center.
