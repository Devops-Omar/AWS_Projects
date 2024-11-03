# AWS Three-Tier Web Application

This project demonstrates the design and deployment of a cost-effective, highly available three-tier web application hosted on AWS. The web tier serves static content, the application tier handles long-running workflows, and the database tier uses Amazon RDS MySQL with minimal management overhead.

## Project Overview

The setup includes:
- **S3 + CloudFront**: Used for serving static web pages globally.
- **ECS Cluster**: Hosts the application tier and runs long-running workflows.
- **Amazon RDS (MySQL)**: Provides a highly available database solution.


![ECS](https://github.com/user-attachments/assets/0dc5f462-3099-441f-bca6-78ad13e57f2d)


# Project Requirements

1. **Web Tier**:
   - Serve static web pages using S3 and CloudFront.
2. **Application Tier**:
   - Run long-running workflows on an ECS cluster.
3. **Database Tier**:
   - Use Amazon RDS with MySQL in a Multi-AZ configuration.
4. **High Availability**:
   - Ensure all tiers are highly available.
5. **Cost-Effective Solution**:
   - Minimize ongoing management and operational overhead.


# Solution Overview

## Three-Tier Architecture
- **Web Tier (S3 + CloudFront)**:
  - Host static web pages on an S3 bucket with CloudFront for global distribution.
- **Application Tier (ECS)**:
  - Deploy ECS containers to handle application workloads.
- **Database Tier (RDS MySQL)**:
  - Use a Multi-AZ Amazon RDS deployment for high availability and reliability.

## High Availability
- S3 with CloudFront ensures global distribution.
- ECS cluster deployed in multiple availability zones for redundancy.
- RDS in a Multi-AZ configuration for database failover.

## Cost-Effectiveness
- Serverless storage (S3) reduces hosting costs.
- Managed ECS and RDS services minimize maintenance efforts.


