# Networking and Security

## 1. Overview

EduCloud uses AWS networking services to connect its frontend and backend environments securely.

## 2. VPC Networking

- Frontend and backend run in separate VPC environments.
- VPC Peering provides private network connectivity.
- Private IP addresses are used for communication between the environments.

## 3. Private IP Configuration

| Component | Reported Private IP |
|---|---|
| Frontend EC2 | 10.0.1.154 |
| Backend EC2 | 10.20.1.124 |

## 4. Nginx Reverse Proxy

Nginx forwards API requests from the frontend domain to the backend application.

Backend target:

`http://10.20.1.124:5000`

## 5. Application Security

- HTTPS is enabled for the public website.
- JWT-based authentication is used.
- Backend APIs validate incoming requests.
- Login requests require email and password.

## 6. Connectivity Validation

Frontend-to-backend communication was verified successfully.

The backend returned HTTP 200 during connectivity testing.

## 7. Security Improvements

- Restrict Security Group access to required ports and trusted sources.
- Keep application secrets outside source code.
- Use least-privilege IAM permissions.
- Monitor authentication and application logs.
- Review network access rules regularly.

## 8. Documentation Scope

Exact Security Group rules, route table entries, subnet CIDRs, and IAM policies have not been independently verified and are not claimed here.
