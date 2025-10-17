# Docsync: Real-Time Collaborative Document Editing Backend

## Overview
Docsync is a real-time backend service built with NestJS that enables collaborative editing of documents by multiple users simultaneously. It leverages PostgreSQL for persistent storage, Redis Pub/Sub for broadcasting live updates, and AWS SQS for background event queueing. Containerized with Docker and integrated with GitHub Actions, it supports development workflows with continuous integration and deployment.

---

## Features
- Modular NestJS monolith with RESTful and WebSocket APIs.
- Persistent document data and versioning in PostgreSQL.
- Real-time updates via Redis Pub/Sub for low-latency collaboration.
- Background processing using AWS SQS for autosave and notifications.
- Dockerized for consistent development and production environments.
- Basic GitHub Actions CI/CD pipeline for automated testing and deployment.

---

## Technologies Used
- NestJS, TypeScript
- PostgreSQL
- Redis Pub/Sub
- AWS SQS
- Docker
- GitHub Actions

---

## Installation & Setup

### Prerequisites
- Node.js v16 or above
- Docker installed locally
- PostgreSQL database accessible
- Redis server up and running
- AWS account with SQS configured
- Proper credentials and environmental variables configured

### Setup Commands
```
git clone https://github.com/yourusername/docsync.git
cd docsync
npm install
```
Create `.env` file with keys:
```
DATABASE_HOST=your_postgres_host
DATABASE_USER=your_db_user
DATABASE_PASS=your_db_password
REDIS_HOST=your_redis_host
AWS_ACCESS_KEY_ID=your_aws_key
AWS_SECRET_ACCESS_KEY=your_aws_secret
SQS_QUEUE_URL=your_sqs_url
```
Run locally:
```
npm run start:dev
```
Using Docker:
```
docker build -t docsync .
docker run -p 3000:3000 docsync
```

---

## Future Enhancements
- Add WebRTC support for peer-to-peer document syncing.
- Implement advanced conflict resolution.
- Integrate Elasticsearch for fast document search.
- Expand CI/CD with automated cloud deployment and monitoring.

---

## Contributing
Open to issues and pull requests for improvements.

---

## License
MIT License
