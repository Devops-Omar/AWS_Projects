![RDS](https://github.com/user-attachments/assets/c1f4c1bf-83f5-4ab3-a238-7e3e30cdef0d)

# AWS High-Availability Database Tier

This project demonstrates the design and implementation of a highly available and fault-tolerant database tier for a multi-tier web application. The solution also supports complex reporting queries without impacting the primary database performance and ensures encryption in transit.

## Project Overview

The setup includes:
- **Highly Available Database**: Multi-AZ RDS deployment for redundancy.
- **Support for Reporting Tools**: Ensures reporting queries do not affect main database performance.
- **Encryption in Transit**: Communication between the application and the database is secured.
- **Minimal Database Overheads**: Designed for minimal ongoing management.

# Project Requirements

1. **Database Design**:
   - Must be highly available and fault tolerant for a multi-tier web application.
2. **Support for Reporting Tools**:
   - The database should handle complex queries without impacting main performance.
3. **Encryption**:
   - Communication between the application and the database must be encrypted in transit.
4. **Performance**:
   - Ensure minimal ongoing database overhead while optimizing for reporting needs.

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
