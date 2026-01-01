# MERN Stack ToDo Web App

### 🎯 Overview
This project demonstrates how to containerize a full-stack three-tier ToDo web application using **Docker & Docker Compose.**
It follows a modern micro-service style architecture with separate services for **frontend, backend, and database.**


### 🧩 App Architecture
| Layer                | Technology             | Description                                 |
| -------------------- | ---------------------- | ------------------------------------------- |
| **Frontend**         | React.js               | User interface for managing ToDo items      |
| **Backend**          | Node.js                | REST API service handling business logic    |
| **Database**         | MongoDB                | Persistent data storage                     |
| **Containerization** | Docker, Docker Compose | Service orchestration and environment setup |


### 🛠️ Prerequisites
| Tool        | Purpose                                                   | Documentation |
|-------------|-----------------------------------------------------------|---------------|
| **Node.js** | JavaScript runtime for backend service | [Install Node.js](https://nodejs.org/en/download) |
| **npm**     | Package manager for installing and managing dependencies | [npm Documentation](https://docs.npmjs.com/) |
| **Docker**  | Builds and runs container images for application services | [Install Docker](https://docs.docker.com/engine/install/) |
| **Kubectl** *(optional for k8s)* | Used to interacting with the Kubernetes API server. | [Install Kubectl CLI](https://kubernetes.io/docs/tasks/tools/) |
| **KIND** *(optional for k8s)* | Used to deploy and test the application locally on Kubernetes | [Install Kind](https://kind.sigs.k8s.io/docs/user/quick-start/) |


### 🧪 Running the Application with Docker Compose
**Step 1 — Build & Start Services**
```sh
docker compose up --build -d
```
**Step 2 — Verify Services**
```sh
docker compose ps
```
**Step 3 — View Logs**
```sh
docker compose logs -f
```
**Step 4 — Access the Application**
Open your browser and navigate to:
```sh
http://localhost:3000
```
![output](/assets/output.png)

**Step 5 — Stop & Clean Up**
```sh
docker compose down -v
```


### 🧾 Summary
- Full-stack ToDo management
- Persistent data using MongoDB volumes
- Isolated services using Docker containers
- Easy setup with single command deployment


### 📚 References
- [Docker Documentation](https://docs.docker.com/)
- [NGINX Ingress Controller](https://kubernetes.github.io/ingress-nginx/)
- [MongoDB on Kubernetes](https://www.mongodb.com/kubernetes)
- [Kubernetes Official Docs](https://kubernetes.io/docs/)
- [KIND Guide](https://kind.sigs.k8s.io/)
