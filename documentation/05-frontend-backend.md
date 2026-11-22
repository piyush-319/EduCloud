# Frontend and Backend Implementation

## 1. Application Overview

EduCloud is a web-based learning platform with a React frontend and Node.js backend.

## 2. Frontend Implementation

### Technology

- React.js
- Nginx
- HTML, CSS and JavaScript

### Responsibilities

- Displays the EduCloud homepage.
- Provides user registration and login interfaces.
- Displays the learning dashboard.
- Provides course and lesson navigation.
- Communicates with backend APIs.

## 3. Backend Implementation

### Technology

- Node.js
- Express.js
- JWT Authentication

### Responsibilities

- Handles user registration and login.
- Provides authentication endpoints.
- Returns course and lesson information.
- Handles learning progress requests.
- Processes password recovery requests.

## 4. Nginx Configuration

Nginx serves the frontend application and acts as a reverse proxy for backend API requests.

Backend API target:

`http://10.20.1.124:5000`

## 5. Authentication Flow

1. User opens the login page.
2. User submits email and password.
3. Backend validates the login request.
4. Backend responds with authentication information.
5. User is redirected to the dashboard after successful login.

## 6. Application Features

- User registration
- User login and logout
- Dashboard
- Course listing
- Lesson navigation
- Learning progress tracking
- Password recovery

## 7. Application URL

https://myeducloud.in

## 8. Implementation Scope

This document describes the currently implemented application features. Additional enhancements will be documented separately under Future Improvements.
