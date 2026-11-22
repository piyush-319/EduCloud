# EduCloud API Documentation

## 1. Overview

EduCloud backend APIs are developed using Node.js and Express.js.

The backend handles authentication, course information, lessons, and learning progress.

## 2. Backend Configuration

- Framework: Express.js
- Runtime: Node.js
- Backend Server: EC2
- Application Port: 5000
- API Base URL: `https://myeducloud.in/api`

## 3. API Endpoints

### Authentication APIs

| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/api/register` | Register a new user |
| POST | `/api/login` | Authenticate a user |
| GET | `/api/me` | Retrieve authenticated user information |
| POST | `/api/forgot-password` | Request password recovery |
| POST | `/api/reset-password` | Reset account password |

### Course APIs

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/api/courses` | Retrieve available courses |
| GET | `/api/courses/:courseId/lessons` | Retrieve lessons for a course |

### Learning Progress APIs

| Method | Endpoint | Purpose |
|---|---|---|
| POST | `/api/progress/:lessonId` | Update lesson progress |
| GET | `/api/progress` | Retrieve learning progress |

### Root Endpoint

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/` | Backend root endpoint |

## 4. API Communication

Frontend API requests are forwarded through Nginx to the backend server.

Backend target:

`http://10.20.1.124:5000`

## 5. API Validation

The following API behavior was verified:

- `GET /api/courses` returned HTTP 200.
- `POST /api/login` returned HTTP 200 for a successful login.
- Login with missing email and password returned HTTP 400.
- Frontend-to-backend connectivity returned HTTP 200.

## 6. Authentication

EduCloud uses JWT-based authentication.

Authentication information is handled by the backend and used by the frontend for protected application access.

## 7. Documentation Scope

Endpoint methods and paths are documented from the backend implementation.

Detailed request bodies, response schemas, and error codes are not included because they have not been fully documented here.
