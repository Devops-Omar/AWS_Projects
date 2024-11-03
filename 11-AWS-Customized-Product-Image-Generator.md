# AWS Customized Product Image Generator

This project demonstrates the design and deployment of a cost-effective, highly available, API-based serverless solution on AWS. The solution allows customers to browse a customizable products catalog and submit customization requests, generating on-demand customized product images. Customers receive a link to view the image before ordering.

## Project Overview

The setup includes:
- **API Gateway**: Front-facing interface for receiving customization requests.
- **AWS Lambda**: Processes customization requests and generates images.
- **S3 Bucket**: Stores the generated images and serves them to customers.
- **CloudFront**: Distributes the images globally for low-latency access.

![Lambda Function](https://github.com/user-attachments/assets/1e2f00cc-a92f-4689-bd38-8e7d5177e4c3)


  # Project Requirements

1. **Serverless Solution**:
   - Must be highly available and scalable.
2. **API-Based Application**:
   - Allow customers to browse images and submit customization requests.
3. **On-Demand Image Generation**:
   - Create customized product images as per customer requests.
4. **Link Generation**:
   - Provide customers with a link to view the customized image.
5. **Cost-Effectiveness**:
   - Ensure the solution is cost-effective.
6. **Scope**:
   - The front-end and database design are out of scope.

# Solution Overview

## Serverless Architecture
- **API Gateway**:
  - Front-end for receiving requests and routing them to Lambda.
- **Lambda Function**:
  - Processes customization requests and generates images.
- **S3 Bucket**:
  - Stores generated images and serves them to customers.
- **CloudFront**:
  - Provides a globally distributed content delivery network for image access.

## Workflow
1. Customer submits a customization request via API Gateway.
2. API Gateway triggers a Lambda function.
3. Lambda processes the request, generates the customized image, and stores it in an S3 bucket.
4. The S3 bucket sends a notification to trigger an SNS topic.
5. The customer receives a URL to view the customized image.

## Cost-Effectiveness
- Serverless model ensures charges are incurred only for actual usage.
- Storage costs are minimized by using S3 with lifecycle policies if necessary.


