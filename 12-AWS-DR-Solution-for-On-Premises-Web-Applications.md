# AWS DR Solution for On-Premises Web Applications

This project demonstrates the design and deployment of a Disaster Recovery (DR) solution for on-premises web applications using AWS. The solution ensures data synchronization between on-premises and AWS, providing a seamless failover mechanism with minimal downtime.

## Project Overview

The setup includes:
- **AWS Storage Gateway**: Facilitates data synchronization between on-premises storage and AWS.
- **Amazon S3**: Stores replicated data securely and efficiently.
- **Route 53**: Configured for failover routing to redirect traffic from on-premises to AWS during failover.
- **VPC Configuration**: Ensures a secure and scalable infrastructure in AWS.


![EFS](https://github.com/user-attachments/assets/18c290f0-e118-4bff-9705-3db6a0ce7875)

# Project Requirements

1. **DR Solution**:
   - Ensure that on-premises and AWS data are kept in sync.
2. **Minimal Downtime**:
   - Failover from on-premises to AWS must have the least possible downtime.
3. **Scalability**:
   - The architecture in AWS should be scalable to handle load during failover.
4. **Data Synchronization**:
   - Use a solution that provides real-time data replication between on-premises and AWS.
5. **Security**:
   - Data transfer must be secure.


# Solution Overview

## DR Solution Architecture
- **Storage Gateway**:
  - Acts as a bridge to sync data between on-premises and AWS.
- **S3 Buckets**:
  - Used as the primary storage for replicated data.
- **Route 53**:
  - Configured for failover routing to switch traffic to AWS during an outage.
- **VPC**:
  - Hosts web servers ready to take over during failover.

## Failover Mechanism
- Route 53 is set up with a failover routing policy to detect failures and redirect traffic to the AWS environment.

## Data Sync
- **AWS Storage Gateway** ensures that data is replicated in real-time from the on-premises storage system to Amazon S3.



