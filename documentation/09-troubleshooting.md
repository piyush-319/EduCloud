# Troubleshooting Guide

## 1. Overview

This document covers common issues that may occur while running and maintaining EduCloud.

## 2. Frontend Issues

### Website Not Loading

Possible areas to check:

- Nginx service status.
- Frontend build files.
- Nginx configuration.
- Domain and HTTPS configuration.

### Frontend API Request Failure

Possible areas to check:

- Nginx reverse proxy configuration.
- Backend server availability.
- Backend private IP address.
- Network connectivity between VPCs.

## 3. Backend Issues

### Backend Not Responding

Check:

- Node.js application status.
- Backend application logs.
- Port 5000 availability.
- Backend server configuration.

### API Returns HTTP 404

Check:

- API endpoint path.
- HTTP request method.
- Express route definitions.

## 4. Networking Issues

### Frontend Cannot Reach Backend

Check:

- VPC Peering connection status.
- Route table configuration.
- Security Group rules.
- Backend private IP address.
- Backend application port.

## 5. Authentication Issues

### Login Failure

Check:

- Email and password input.
- Backend login endpoint.
- Authentication response.
- Browser network errors.

## 6. Useful Diagnostic Commands

Check Nginx status:

`sudo systemctl status nginx`

Test Nginx configuration:

`sudo nginx -t`

Check listening ports:

`sudo ss -tulnp`

Check backend connectivity:

`curl -I http://10.20.1.124:5000`

## 7. Documentation Scope

The commands above are diagnostic references. They do not imply that every listed issue occurred during the project deployment.
