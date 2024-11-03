# AWS Video Transcoding Application

This project demonstrates the design and deployment of a web-based video transcoding application using AWS. The solution includes both free and paid tiers, where the paid tier receives priority service. The application stores uploaded and transcoded videos in scalable, durable storage and handles notifications to users once jobs are completed.

## Project Overview

The setup includes:
- **S3 Buckets**: For uploading and storing transcoded videos.
- **SQS Queues**: Separate queues for free and paid tiers.
- **Lambda Functions**: For processing video transcoding requests.
- **SNS**: For sending notifications when jobs are completed.
- **DynamoDB**: Optional for tracking user activity and job status.


![Notifications](https://github.com/user-attachments/assets/dd143c52-f0a8-4c5d-a619-ffc7f9f3c3c8)

# Project Requirements

1. **Video Transcoding Solution**:
   - Must support both free and paid tiers.
2. **Priority Service for Paid Tier**:
   - Paid tier must have scalable processing based on job queue size.
3. **Scalable and Durable Storage**:
   - Use Amazon S3 for uploaded and transcoded videos.
4. **Decoupled Application Tiers**:
   - Ensure the frontend and backend are decoupled for scalability.
5. **User Notifications**:
   - Notify users by email when their jobs are completed.
6. **Minimal Operational Overhead**:
   - Use managed services to minimize ongoing management efforts.

# Solution Overview

## Architecture Overview
- **Storage (S3 Buckets)**:
  - Used for storing uploaded videos and transcoded output.
- **Queues (SQS)**:
  - Separate queues for handling free and paid tier video jobs.
- **Lambda Functions**:
  - Process video transcoding requests and move output to S3.
- **Notifications (SNS)**:
  - Sends email notifications to users once transcoding is complete.

## Scalable Design
- Utilizes SQS to handle spiky traffic and decouple job processing.
- Auto-scaling mechanisms in place for paid tier backend based on queue size.


