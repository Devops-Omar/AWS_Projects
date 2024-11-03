# AWS Active-Active Database Design

This project demonstrates the design and deployment of a highly available, active-active database tier for an e-commerce application. The application is distributed across two AWS regions, providing consistent low-latency performance and real-time data replication.

## Project Overview

The setup includes:
- **Regions**: US-East-1 and EU-West-1 for active-active deployment.
- **Database**: DynamoDB Global Tables to ensure low-latency read and write operations in both regions.
- **Replication**: Near real-time data replication between regions.
- **Scalability**: Designed to scale seamlessly without downtime.
- **Flexible Schema**: Supports evolving data structures as needed by the development team.


![DynamoDB](https://github.com/user-attachments/assets/b51866cc-a015-4c23-ba60-6c7822a40de7)

# Project Requirements

1. **Deployment**:
   - The application is deployed in US-East-1 and EU-West-1 in an active-active configuration.
2. **Performance**:
   - Database must provide consistent single-digit millisecond latency at any scale.
3. **Replication**:
   - New item writes to one region must be replicated to the other within one second.
4. **Read and Write Support**:
   - Both regions must support read and write operations.
5. **Management**:
   - The database must be managed by AWS (no manual management required).
6. **Schema Flexibility**:
   - The database must support a flexible schema to accommodate evolving data needs.
7. **Scalability**:
   - The database should scale without downtime to handle increased load.
  
   # Solution Overview

## Active-Active Configuration
- **DynamoDB Global Tables** are used to deploy the database in US-East-1 and EU-West-1, supporting read and write operations in both regions.
- Real-time replication ensures that data is consistently updated within one second between the two regions.

## Performance
- DynamoDB provides single-digit millisecond latency for both reads and writes at any scale.

## Scalability
- **Auto-Scaling**:
  - DynamoDB's auto-scaling feature ensures that the database scales based on the application's load without downtime.

## Schema Flexibility
- DynamoDB supports a **NoSQL** flexible schema model, allowing the development team to adapt data structures as the application evolves.


