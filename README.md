<p align="center">
  <img src="./EduCloud%20Neon%20Wave%20Animation%20%281.5x%29.gif" alt="EduCloud Banner" width="100%">
</p>

---

## 🌐 Live Project

**Website:** https://myeducloud.in

**GitHub Repository:** https://github.com/piyush-319/EduCloud

**Docker Hub:** https://hub.docker.com/r/piyush200331/educloud

---

## 🚀 Project Overview

EduCloud is a full-stack learning platform developed to combine web development with cloud computing and DevOps practices.

The project includes:

- React frontend for the user interface.
- Node.js and Express backend for API services.
- PostgreSQL for database management.
- AWS EC2 for application hosting.
- Nginx for frontend hosting and reverse proxy.
- Docker for application containerization.
- GitHub Actions workflows for CI.

flowchart TB
    U["Users"] --> D["myeducloud.in"]
    
    subgraph FV["Frontend VPC - 10.0.0.0/16"]
        FE["Frontend EC2"]
        N["Nginx"]
        R["React Application"]
        FE --> N --> R
    end

    subgraph BV["Backend VPC - 10.20.0.0/16"]
        BE["Backend EC2 - 10.20.1.124"]
        API["Node.js + Express API"]
        DB[("Amazon RDS - PostgreSQL")]
        BE --> API --> DB
    end

    D --> FE
    N -->|" /api/ requests "| API
    style FV fill:#e8f2ff,stroke:#3676b8
    style BV fill:#eaf7ed,stroke:#39844b

---

## ✨ Key Features

- Modern React-based frontend.
- REST API powered by Node.js and Express.
- PostgreSQL database integration.
- User authentication and authorization.
- Course and lesson management.
- Student progress tracking.
- Password reset functionality.
- AWS-based application hosting.
- Dockerized frontend and backend images.

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Frontend | React, JavaScript, CSS, Vite |
| Backend | Node.js, Express.js |
| Database | PostgreSQL, Amazon RDS |
| Cloud | AWS EC2, VPC, IAM |
| Web Server | Nginx |
| Containers | Docker |
| CI | GitHub Actions |
| Version Control | Git, GitHub |

---

## ☁️ AWS Infrastructure

EduCloud uses AWS infrastructure to host and connect its application components.

- **Amazon EC2:** Hosts frontend and backend services.
- **Amazon VPC:** Provides network isolation.
- **Public and Private Subnets:** Separate network environments.
- **Security Groups:** Control inbound and outbound traffic.
- **Amazon RDS:** Hosts the PostgreSQL database.
- **Nginx:** Serves the frontend and forwards API requests.
- **AWS Systems Manager:** Supports instance management.

---

## 🐳 Docker Hub Images

Docker images are available on Docker Hub.

| Component | Docker Image |
|---|---|
| Frontend | `piyush200331/educloud:frontend-v1` |
| Backend | `piyush200331/educloud:backend-v2` |

### Pull Frontend Image

```bash
docker pull piyush200331/educloud:frontend-v1
```

### Pull Backend Image

```bash
docker pull piyush200331/educloud:backend-v2
```

**Docker Hub:** https://hub.docker.com/r/piyush200331/educloud

---

## 📁 Project Structure

```text
EduCloud/
│
├── frontend/
│   ├── public/
│   ├── src/
│   ├── Dockerfile
│   ├── package.json
│   └── README.md
│
├── backend/
│   ├── server.js
│   ├── Dockerfile
│   ├── package.json
│   └── package-lock.json
│
├── .github/
│   └── workflows/
│
├── .gitignore
└── README.md
```

---

## 💻 Run Locally

### 1. Clone Repository

```bash
git clone https://github.com/piyush-319/EduCloud.git
cd EduCloud
```

### 2. Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

### 3. Backend Setup

Open another terminal:

```bash
cd EduCloud/backend
npm install
```

Configure the required environment variables in a local `.env` file, then start the backend:

```bash
npm start
```

**Note:** Database credentials, JWT secrets, and email credentials must be configured locally. Never commit `.env` files to GitHub.

---

## 🔄 CI Workflows

GitHub Actions workflows are included for frontend and backend:

- Frontend CI workflow
- Backend CI workflow

These workflows help automate checks when code is pushed to GitHub.

---

## 🎯 Project Goals

- Learn practical AWS cloud infrastructure.
- Understand VPC networking and subnet architecture.
- Implement frontend and backend integration.
- Practice Docker image creation and publishing.
- Understand CI workflows using GitHub Actions.
- Build and maintain a real-world cloud-hosted application.

---

## 👨‍💻 Author

**Piyush Bandre**

Electronics & Telecommunications | Cloud Computing | AWS | Linux | DevOps

GitHub: https://github.com/piyush-319

---

<p align="center">
  <b>EduCloud – Building a smarter learning experience with cloud technology ☁️</b>
</p>

