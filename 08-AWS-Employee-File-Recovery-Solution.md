# AWS Employee File Recovery Solution

This project demonstrates the design and implementation of a cost-effective, scalable, and highly durable file recovery solution for employee home directories using AWS S3 storage with lifecycle management.

## Project Overview

The setup includes:
- **S3 Standard** for immediate data access within the first 30 days.
- **S3 Standard-IA (Infrequent Access)** for data access between 30 and 75 days.
- **S3 Glacier Deep Archive** for long-term storage and recovery within 48 hours after 75 days, up to 9 months.
- **Lifecycle Policy** to transition data through these storage classes automatically.
- 
![S3](https://github.com/user-attachments/assets/1af08eb8-88ac-452c-b7b3-1cd3dd73d068)

# Project Requirements

1. **Storage Solution**:
   - Must be highly available and durable.
   - Must be cost-effective.
2. **Immediate Recovery**:
   - Employees should be able to recover their deleted files within the first 75 days.
3. **Long-Term Recovery**:
   - Recovery of deleted files must be possible up to 9 months after deletion, with a recovery time of 48 hours.
4. **Scalability**:
   - The solution should scale with the organization’s growth and data volume.
  
   # Solution Overview

## Storage Class Lifecycle
- **S3 Standard**:
  - Used for immediate data access for the first 30 days.
- **S3 Standard-IA**:
  - Used for data access between 30 to 75 days.
- **S3 Glacier Deep Archive**:
  - Used for long-term storage beyond 75 days, with recovery available within 48 hours.

## Cost-Effectiveness
- Transitioning objects to colder storage classes like **Standard-IA** and **Glacier Deep Archive** helps reduce costs.

## Data Recovery Process
- **Immediate Recovery**:
  - Files can be recovered directly from **S3 Standard** and **Standard-IA** within 75 days.
- **Long-Term Recovery**:
  - Files stored in **S3 Glacier Deep Archive** can be restored within 48 hours upon request.



