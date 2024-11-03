# AWS Cloud Bursting Solution

This project demonstrates the design and implementation of a cloud bursting solution to extend an on-premises multi-tier application into AWS whenever additional capacity is needed. The architecture is scalable and highly available, with an on-premises database serving both environments over an existing Direct Connect link.

## Project Overview

The setup includes:
- **On-Premises to AWS Extension**: AWS acts as an overflow for on-premises resources during peak demand.
- **Direct Connect**: Ensures a high-bandwidth, low-latency connection between on-premises and AWS.
- **Scalable and Highly Available Architecture**: Leverages AWS services to extend capacity.
- **Weighted Routing Policy**: Manages traffic distribution between on-premises and AWS.

 ![53-CloudFront](https://github.com/user-attachments/assets/f340cd72-8f29-4f66-960a-fced8026832d)


# Project Requirements

1. **Cloud Bursting Solution**:
   - Extend on-premises multi-tier applications into AWS for additional capacity.
2. **Scalability and High Availability**:
   - AWS architecture must be scalable and resilient.
3. **Direct Connect**:
   - Use an existing Direct Connect for communication between on-premises and AWS.
4. **Traffic Management**:
   - Route traffic between on-premises and AWS using weighted routing policies.
5. **Database Tier**:
   - On-premises database must serve both environments over Direct Connect.

# Solution Overview

## Cloud Bursting Architecture
- **VPC Setup**:
  - Create a VPC with public and private subnets across multiple availability zones for high availability.
- **Direct Connect**:
  - Use Direct Connect to link on-premises infrastructure with AWS.
- **Routing Policy**:
  - Implement Route 53 weighted routing to manage traffic flow between the on-premises data center and AWS.

## High Availability
- Deploy instances in multiple availability zones to ensure that the AWS environment is fault-tolerant.

## Traffic Management
- Use weighted routing to dynamically control traffic distribution based on capacity and demand.

