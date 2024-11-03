# AWS User Storage Monitoring Solution

This project demonstrates the design and deployment of an AWS-based object storage solution that supports a free tier with a 5GB storage limit and a paid tier with a 100GB storage limit. The solution includes user storage tracking and automated notifications when storage usage reaches specific thresholds.

## Project Overview

The setup includes:
- **S3 Bucket**: Stores user files and triggers notifications on object uploads.
- **DynamoDB**: Tracks user storage usage.
- **SQS and SNS**: Used for sending notifications when users reach 80% and 95% of their storage limits.
- **Automation**: Integrated notification system alerts users at specific thresholds.

  ![S3_3](https://github.com/user-attachments/assets/3878f0d7-38dd-4215-b15b-e16792da7c55)

  # Project Requirements

1. **Storage Limits**:
   - Free tier with a 5GB limit and a paid tier with a 100GB limit.
2. **User Storage Tracking**:
   - Real-time tracking of each user’s storage activities.
3. **Notification System**:
   - Send notifications when users reach 80% and 95% of their storage limits.
4. **Scalability**:
   - Must support growing user data without manual intervention.
5. **Cost-Effectiveness**:
   - The solution should be cost-effective while maintaining high availability and durability.
  
     # Solution Overview

## Storage Solution
- **S3 Bucket**:
  - Central storage location for user data.
- **DynamoDB**:
  - Used to store and track user storage usage data.
- **S3 Event Notifications**:
  - Configured to trigger notifications on object uploads to update the user’s storage data in DynamoDB.

## Notification System
- **SQS and SNS Integration**:
  - SQS processes notifications, and SNS sends alerts when storage thresholds (80% and 95%) are reached.

## Scalability and Cost-Effectiveness
- Leveraging managed AWS services ensures the solution scales with user growth and optimizes costs.



