3-Tier E-commerce Application
Live Application
Frontend URL: http://18.207.123.74:3000
Backend API: http://18.207.123.74:8080

Project Overview
A fully deployed 3-tier e-commerce web application with automated CI/CD pipeline running on AWS EC2.

Architecture
Frontend: React.js (Port 3000)
Backend: Node.js/Express.js (Port 8080)
Database: PostgreSQL (Port 5432)
Infrastructure: AWS EC2 Ubuntu + Docker
Repository Structure
text

├── bezkoder-ui/ # React Frontend
│ ├── src/
│ ├── Dockerfile
│ └── package.json
├── bezkoder-api/ # Node.js Backend
│ ├── .env
│ ├── Dockerfile
│ └── package.json
├── docker-compose.yml # Multi-container setup
└── .github/workflows/
└── ci-cd.yml # CI/CD Pipeline

Quick Deployment
Prerequisites
AWS EC2 Ubuntu instance
Docker & Docker Compose
GitHub repository with secrets configured
Manual Deployment
bash

Clone repository
git clone https://github.com/malikfaisal11/react-nodejs-mysql-three--tier-app.git
cd react-nodejs-mysql-three--tier-app

Deploy all services
docker-compose up -d

Check status
docker-compose ps

CI/CD Pipeline
GitHub Actions automatically:

Builds Docker images on push to main branch
Pushes images to Docker Hub
Deploys updates to EC2 instance
Pipeline Status
https://github.com/your-username/your-repo/actions/workflows/ci-cd.yml/badge.svg

Access Points
Web Application: http://18.207.123.74:3000
Backend API: http://18.207.123.74:8080/api
Database: PostgreSQL@18.207.123.74:5432
Features
3-Tier Architecture
Docker Containerization
Automated CI/CD
PostgreSQL Database
RESTful APIs
React Frontend
Troubleshooting
bash

View logs
docker-compose logs

Restart services
docker-compose restart

Check container status
docker-compose ps