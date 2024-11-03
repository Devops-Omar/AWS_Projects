# AWS High-Availability Database Tier Solution

This project demonstrates the design and deployment of a highly available, fault-tolerant database tier for a multi-tier web application. The setup ensures reporting queries do not impact the primary database performance and includes encryption in transit to maintain security.

## Project Overview

The setup includes:
- **Highly Available Database**: Multi-AZ RDS deployment with read replicas.
- **Reporting Optimization**: Separation of reporting queries to ensure minimal impact on the primary database.
- **Encryption**: Data in transit between the application and the database is encrypted.
- **Minimal Overheads**: The solution is designed to reduce ongoing maintenance and overhead.

![RDS](https://github.com/user-attachments/assets/c1f4c1bf-83f5-4ab3-a238-7e3e30cdef0d)

# Project Requirements

1. **Database Tier Design**:
   - Must be highly available and fault-tolerant for a multi-tier web application.
2. **Support for Reporting Tools**:
   - Ensure that reporting queries run against the database without impacting its primary performance.
3. **Encryption in Transit**:
   - Implement SSL/TLS for encrypted data transfer between the application and the database.
4. **Minimal Ongoing Overheads**:
   - Optimize the design to reduce maintenance.

# Solution Overview

## High Availability
- **RDS Configuration**:
  - Deploy an RDS instance with Multi-AZ configuration to ensure continuous database availability.
- **Redundancy**:
  - The primary database will be backed by a standby in a separate availability zone.

## Performance Optimization
- **Read Replicas**:
  - Deploy read replicas or a dedicated reporting instance to handle reporting tool queries.
- **Load Distribution**:
  - Direct reporting queries to the read replicas to reduce load on the primary database.

## Encryption
- **SSL/TLS Configuration**:
  - Enable SSL/TLS for data in transit between the web/application tier and the database.
