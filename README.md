<p align="center">
  <img src="./EduCloud%20Neon%20Wave%20Animation%20%281.5x%29.gif" alt="EduCloud Banner" width="100%">
</p>

---

## 🎬 Project Demo

https://github.com/user-attachments/assets/9e54db13-2000-4afd-b955-5a5da6b6124e

---

## 🌐 Live Project

**Website:** https://myeducloud.in  
**GitHub Repository:** https://github.com/piyush-319/EduCloud         https://github.com/Mahek-319  
**Docker Hub:** https://hub.docker.com/r/piyush200331/educloud        https://hub.docker.com/r/mahek19/educloud

---

## 🚀 Project Overview

EduCloud is a collaborative full-stack learning platform built to combine web development with AWS cloud infrastructure and foundational DevOps practices.

The platform includes:
- React frontend for the user interface.
- Node.js and Express backend for API services.
- PostgreSQL database integration; current AWS database deployment status is not independently verified.
- AWS EC2 instances in separate frontend and backend VPC environments.
- Nginx for frontend hosting and API reverse proxy.
- Docker images for frontend and backend applications.
- GitHub Actions workflows for frontend build and backend checks.

## ✨ Key Features

- React-based learning platform interface.
- REST APIs powered by Node.js and Express.
- PostgreSQL database integration.
- User authentication and authorization.
- Course and lesson management.
- Student progress tracking.
- Password reset functionality.
- AWS-based application hosting.
- Dockerized frontend and backend images.

---

## 👥 Project Contributors

EduCloud was developed collaboratively by two contributors. The responsibilities below describe each contributor's main areas of work.

### Mahek Gupta — Frontend Developer & AWS Infrastructure Contributor

GitHub: https://github.com/Mahek-319

- Designed and developed the React frontend.
- Worked on website UI, page layout and user experience.
- Contributed one lesson to the backend learning content.
- Collaborated on AWS infrastructure setup and cloud networking, including EC2, VPCs, subnets and Security Groups.

### Piyush Bandre — AWS & DevOps / Backend Contributor

GitHub: https://github.com/piyush-319

- Designed and structured the learning lessons.
- Contributed one lesson to the backend learning content.
- Collaborated on AWS EC2 infrastructure, VPCs, subnets and Security Groups.
- Configured Nginx, domain routing and HTTPS.
- Worked on backend hosting and PostgreSQL/RDS connectivity.
- Created Dockerfiles, built Docker images and published them to Docker Hub.
- Managed the project repository and Docker image publishing workflow.

Both contributors collaborated on the planning, development and improvement of EduCloud. GitHub collaborator access is enabled for the shared repository.

---

## 🏗️ AWS Architecture

EduCloud uses separate AWS VPC environments for frontend and backend application components.

### Frontend Environment
- Frontend VPC CIDR: 10.0.0.0/16
- Public subnet: 10.0.1.0/24
- Ubuntu EC2 instance hosts the React frontend.
- Nginx serves the frontend and forwards API requests to the backend.
- Domain myeducloud.in is configured with HTTPS.

### Backend Environment
- Backend VPC CIDR: 10.20.0.0/16
- Private subnet: 10.20.1.0/24
- Ubuntu EC2 instance runs the Node.js/Express backend.
- Backend database connectivity details are not included in the currently verified AWS infrastructure documentation.

### AWS Services
- **Amazon EC2:** Hosts frontend and backend services.
- **Amazon VPC:** Provides network isolation.
- **Public and Private Subnets:** Separate application network placement.
- **Security Groups:** Control traffic between application components.
- **Amazon RDS:** Database deployment status is not independently verified.
- **Nginx:** Serves the frontend and forwards API requests.
- **AWS Systems Manager:** Supports instance management.

---

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Frontend | React, JavaScript, CSS, Vite |
| Backend | Node.js, Express.js |
| Database | PostgreSQL (RDS deployment status not verified) |
| Cloud | AWS EC2, VPC, IAM, Security Groups |
| Web Server | Nginx |
| Containers | Docker, Docker Hub |
| CI | GitHub Actions |
| Version Control | Git, GitHub |
| Operating System | Ubuntu Linux |

---

## 🐳 Docker Hub Images

Docker images have been built and published to Docker Hub.

| Component | Docker Image |
|---|---|
| Frontend | piyush200331/educloud:frontend-v1 |
| Backend | piyush200331/educloud:backend-v2 |

### Pull Frontend Image

    docker pull piyush200331/educloud:frontend-v1

### Pull Backend Image

    docker pull piyush200331/educloud:backend-v2

**Docker Hub:** https://hub.docker.com/r/piyush200331/educloud

**Containerization status:** Both images have been built and pushed. The frontend image has been run and tested separately. The backend image has not been deployed as a Docker container to the backend EC2 instance. The live application continues to use its existing host-based Nginx and systemd backend service.

---

## 🔄 GitHub Actions CI

GitHub Actions workflow files are present in the repository:

- .github/workflows/frontend-ci.yml — installs dependencies and builds the React frontend.
- .github/workflows/backend-ci.yml — installs dependencies and checks backend JavaScript syntax.

These are CI workflows. Automated Docker publishing and deployment (CD) are not yet configured. Workflow execution can be checked in the repository's Actions tab.

---

## 🗺️ Project Status & Next Steps

| Area | Status |
|---|---|
| Frontend design and development | Completed |
| Backend development | Completed |
| PostgreSQL and Amazon RDS integration | Not independently verified |
| AWS EC2 and VPC infrastructure | Configured |
| Nginx, domain and HTTPS | Configured |
| Docker images built and pushed | Completed |
| Frontend Docker container test | Completed |
| Backend Docker deployment | Not completed |
| GitHub Actions CI workflows | Passed — frontend build and backend syntax checks |
| Automated CD / Docker image publishing | Planned |
| Terraform – Infrastructure as Code | Planned |

### Planned Improvements

- Extend GitHub Actions to automate Docker image build and publishing.
- Design a safe CI/CD deployment workflow.
- Use Terraform to define and manage AWS infrastructure as code.
- Review existing AWS resources before importing or managing them with Terraform; avoid accidental recreation of live resources.

---

## 📚 Documentation

Detailed project documentation, architecture diagrams and application screenshots are available in the [Documentation Index](documentation/README.md).

## 📁 Project Structure

```text
EduCloud/
├── documentation/
│   ├── 01-project-overview.md
│   ├── 02-aws-architecture.md
│   ├── 03-aws-infrastructure.md
│   ├── 04-networking-security.md
│   ├── 05-frontend-backend.md
│   ├── 06-api-documentation.md
│   ├── 07-docker-implementation.md
│   ├── 08-testing-validation.md
│   ├── 09-troubleshooting.md
│   ├── 10-cost-optimization.md
│   ├── 11-future-improvements.md
│   ├── README.md
│   └── assets/
│       ├── architecture/
│       │   └── educloud-aws-architecture.png
│       └── screenshots/
│           ├── 01-homepage.png
│           ├── 02-learning-paths.png
│           ├── 03-why-educloud.png
│           ├── 04-projects.png
│           ├── 05-login.png
│           └── 06-registration.png
├── .github/
│   └── workflows/
│       ├── frontend-ci.yml
│       └── backend-ci.yml
├── frontend/
│   ├── public/
│   ├── src/
│   ├── Dockerfile
│   ├── package.json
│   └── package-lock.json
├── backend/
│   ├── server.js
│   ├── Dockerfile
│   ├── package.json
│   └── package-lock.json
├── .gitignore
└── README.md
```

---

## 💻 Run Locally

### 1. Clone Repository

    git clone https://github.com/piyush-319/EduCloud.git
    cd EduCloud

### 2. Frontend Setup

    cd frontend
    npm install
    npm run dev

### 3. Backend Setup

Open another terminal:

    cd EduCloud/backend
    npm install
    npm start

Configure the required environment variables in a local .env file before starting the backend.

**Note:** Database credentials, JWT secrets and email credentials must be configured locally. Never commit .env files or secrets to GitHub.

---

## 🎯 Project Learning Outcomes

- Practical AWS EC2 instance management.
- VPC, subnet and Security Group concepts.
- Frontend and backend application integration.
- Linux server administration on Ubuntu.
- Nginx hosting and reverse proxy configuration.
- PostgreSQL and Amazon RDS connectivity.
- Dockerfile creation and image publishing.
- GitHub collaboration and CI workflow fundamentals.

---

<p align="center">
  <b>EduCloud – Building a smarter learning experience with cloud technology ☁️</b>
</p>
