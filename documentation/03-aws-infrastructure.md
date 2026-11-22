# AWS Infrastructure

## 1. Overview

EduCloud uses Amazon EC2 instances to host its frontend and backend applications.

## 2. EC2 Instances

### Frontend EC2

- Purpose: Hosts the EduCloud frontend.
- Technology: React.js and Nginx.
- Reported Private IP: `10.0.1.154`

### Backend EC2

- Purpose: Handles backend API requests.
- Technology: Node.js and Express.
- Application Port: `5000`
- Reported Private IP: `10.20.1.124`

## 3. Virtual Private Cloud (VPC)

The frontend and backend environments are hosted in separate VPC environments.

VPC Peering is used to enable private communication between these environments.

## 4. Network Connectivity

- Frontend communicates with the backend using its private IP.
- Nginx acts as a reverse proxy for API requests.
- Backend API connectivity was verified with HTTP 200.

## 5. Infrastructure Scope

This documentation describes the currently reported project setup.

Exact VPC IDs, subnet CIDRs, Availability Zones, and EC2 instance types are not included because they have not yet been verified.

## 6. Future Improvements

- Infrastructure as Code using Terraform.
- Automated infrastructure monitoring.
- Improved resource and cost management.
