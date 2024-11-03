# AWS CloudFormation Centralized Deployment

This project demonstrates a solution for using AWS CloudFormation to centralize infrastructure deployments while ensuring security through least privilege access. The design centralizes deployment to a team of Cloud Administrators and enforces robust access controls as per the Chief Information Security Officer's guidelines.

## Project Overview

The solution includes:
- **Centralized CloudFormation Deployment**: Managed through designated Cloud Administrators.
- **IAM Policies**: Configured to maintain the least privilege principle.
- **Template Storage**: Uses S3 buckets for storing CloudFormation templates.
- **Stack Deployment**: Controlled and secure deployment to different departments.

![Governance](https://github.com/user-attachments/assets/44390516-44d6-499d-a89d-33783c4d6f7d)

# Project Requirements

1. **Centralized CloudFormation Deployment**:
   - Managed by a dedicated team of Cloud Administrators.
2. **Security**:
   - Maintain least privilege access for all deployment activities.
3. **Resource Deployment**:
   - Support the deployment of various resources needed by different departments.


# Solution Overview

## Architecture Design
- **CloudFormation**:
  - Centralized deployment of infrastructure using CloudFormation.
- **IAM Policies**:
  - Created with least privilege to ensure secure access.
- **Template Storage**:
  - Stored in S3 with access controlled by IAM policies.

## Security and Least Privilege
- **IAM Roles**:
  - Specific roles created for Cloud Administrators with minimal permissions.
- **Controlled Access**:
  - Policies that limit permissions to deploy specific resources only.

## Process Flow
1. **Upload Template to S3**.
2. **Deploy Stack via CloudFormation**.
3. **Access Control**:
   - Only Cloud Administrators can deploy stacks.



