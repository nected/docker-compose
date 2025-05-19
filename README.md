# 🚀 Nected Platform - Docker Compose Setup

This repository provides Docker Compose files to help you run a local instance of the **Nected Platform** effortlessly.

---

## 📋 Prerequisites

Before you begin, ensure the following are installed:

- [Docker](https://docs.docker.com/engine/installation/)
- [Docker Compose](https://docs.docker.com/compose/install/)

---

## 🛠️ Getting Started

Follow these steps to set up Nected locally using the default configuration (`docker-compose.yml`):

```bash
# Clone the repository
git clone https://github.com/nected/docker-compose.git

# Navigate to the project directory
cd docker-compose

# Start the containers
docker-compose up
```

### 🌐 Accessing the Application
Once the services are up:
- Open your browser and go to: http://localhost:3000
- Login credentials:
```
Email: dev@nected.local
Password: devPass123
```

### 🔗 API Access Note
When accessing rule or workflow APIs from other services, use the following endpoint format:
```
http://localhost:8002/
```
**Note** Do not use http://10.10.0.1:8002/

---
## 🧰 Troubleshooting
### 🖥️ Apple M4 (ARM) Compatibility
If you're using a Mac with Apple Silicon (M4/M3/M2), you must update JVM options for Elasticsearch.

Steps:
1. Open the .env file located in the root of the docker-compose folder.
2. Uncomment the following two lines (around line 10–11):
```
ES_JAVA_OPTS="-Xms512m -Xmx512m -XX:UseSVE=0"
ES_CLI_JAVA_OPTS="-XX:UseSVE=0"
```
3. Save the file and re-run:
```
docker-compose up
```
###  🌐 Connecting to Local APIs/Databases
To integrate your local APIs or databases with Nected:
- Use your machine's IP address instead of localhost in API/database connection URLs.
- Example: Use http://192.168.x.x:5000 instead of http://localhost:5000

---
## 🤝 Community & Support
For questions, feedback, or contributions:
- Visit our [documentation](https://docs.nected.ai/)
- Join the conversation on [LinkedIn](https://www.linkedin.com/company/nected-ai/)
- Contact the team via support@nected.ai