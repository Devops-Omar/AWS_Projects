# AWS Two-Tier Web Application Security Solution

This project outlines a security solution for a two-tier web application hosted on AWS across two Availability Zones. The solution aims to detect and remediate threats automatically, enhance security posture, and minimize the impact of DDoS and other internet-sourced attacks.

## Project Overview

The solution includes:
- **Web Application Protection**: Using AWS WAF and CloudFront.
- **Threat Detection**: Implemented with Amazon GuardDuty.
- **Automated Remediation**: Utilizes EventBridge and Lambda.
- **Notifications**: Administrators receive alerts via Amazon SNS.

![Security](https://github.com/user-attachments/assets/6459d7cb-dc0d-42a3-b712-b13aab44c2d0)

# Project Requirements

1. **Two-Tier Web Application**:
   - Deployed across two Availability Zones.
2. **Web Application Firewall (WAF)**:
   - Integrated with CloudFront.
3. **Threat Detection and Remediation**:
   - Automated detection using GuardDuty.
   - Event-based remediation using EventBridge and Lambda.
4. **Notifications**:
   - Alerts sent to administrators via SNS.
5. **Cost-Effective and Low Overhead**:
   - The solution must be efficient with minimal operational overhead.
  
   # Solution Overview

## Architecture Design
- **AWS WAF**:
  - Configured to filter out malicious traffic at CloudFront.
- **Amazon GuardDuty**:
  - Monitors and triggers alerts for suspicious activity.
- **EventBridge and Lambda**:
  - Automates threat response by updating the WAF rules.
- **Notifications**:
  - SNS sends out email alerts for detected threats.

## Key Components
- **CloudFront**:
  - Acts as the distribution layer for content.
- **WAF**:
  - Blocks potential threats based on predefined rules.
- **GuardDuty**:
  - Detects and reports potential security threats.
- **SNS**:
  - Notifies administrators of incidents.

## Workflow
1. **Traffic reaches CloudFront**.
2. **AWS WAF filters traffic** based on rules.
3. **GuardDuty monitors and identifies threats**.
4. **EventBridge triggers Lambda** to adjust WAF as needed.
5. **SNS sends notifications** to administrators.







