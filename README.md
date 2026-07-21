# 🐳 Docker Swarm Clustering for Containerized Application Deployment

<p align="center">
  <img src="https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png" alt="Docker Logo" width="140">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Docker-Containers-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Docker%20Swarm-Orchestration-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3.9-blue?style=for-the-badge&logo=python" />
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" />
</p>

---

# 📖 About

This repository demonstrates the deployment of a **containerized machine learning application** using **Docker Swarm**.

The project showcases modern **DevOps practices** by packaging the application into Docker containers, orchestrating them with Docker Swarm, enabling service scaling, configuring networking, and validating fault tolerance through node failure simulation.

The deployment uses a **Docker Swarm Cluster** consisting of:

- 🖥️ 1 Manager Node
- 🖥️ 2 Worker Nodes

The application is deployed as Swarm services with built-in load balancing and high availability.

---

# 🎯 Objectives

- ✅ Containerize the application using Docker
- ✅ Build and manage Docker images
- ✅ Configure a Docker Swarm cluster
- ✅ Deploy services using Docker Compose
- ✅ Enable service discovery and networking
- ✅ Scale application services
- ✅ Demonstrate load balancing
- ✅ Test fault tolerance during node failures

---

# ✨ Features

- 🐳 Docker Containerization
- ☸️ Docker Swarm Cluster
- 📦 Multi-Service Deployment
- 🌐 Overlay Networking
- ⚖️ Automatic Load Balancing
- 📈 Horizontal Scaling
- 🔄 Self-Healing Services
- 💥 Fault Tolerance Testing

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| 🐳 Docker | Containerization |
| ☸️ Docker Swarm | Container Orchestration |
| 🐍 Python 3.9 | Backend Application |
| 📓 Jupyter Notebook | ML Development Environment |
| 📄 Docker Compose | Multi-service Deployment |

---

# 📂 Project Structure

```text
Docker-swarm-clustering--VSS/
│
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── app/
├── notebooks/
├── screenshots/
├── README.md
└── LICENSE
```

---

# 🏗️ Architecture

```text
                    Docker Swarm Cluster

               ┌──────────────────────┐
               │    Manager Node      │
               │  Swarm Management    │
               └──────────┬───────────┘
                          │
          ┌───────────────┴───────────────┐
          │                               │
┌────────────────────┐          ┌────────────────────┐
│    Worker Node 1   │          │    Worker Node 2   │
│  Running Services  │          │  Running Services  │
└────────────────────┘          └────────────────────┘

             Overlay Network
                    │
                    ▼
        Containerized ML Application
```

---

# 🚀 Getting Started

## Clone the Repository

```bash
git clone https://github.com/<your-username>/Docker-swarm-clustering--VSS.git
```

```bash
cd Docker-swarm-clustering--VSS
```

---

# 🐳 Build the Docker Image

```bash
docker build -t pothole_detection .
```

---

# ▶️ Run the Container

```bash
docker run -p 8888:8888 pothole_detection
```

The Jupyter Notebook server will be available at:

```
http://localhost:8888
```

---

# ☸️ Initialize Docker Swarm

```bash
docker swarm init
```

Verify the manager node:

```bash
docker node ls
```

---

# 📦 Deploy the Stack

Deploy using Docker Compose:

```bash
docker stack deploy -c docker-compose.yml ml-stack
```

Verify services:

```bash
docker service ls
```

---

# 📈 Scale Services

Increase replicas:

```bash
docker service scale ml-stack_app=3
```

Verify replicas:

```bash
docker service ps ml-stack_app
```

Docker Swarm automatically distributes containers across available worker nodes.

---

# ⚖️ Load Balancing

Docker Swarm provides built-in load balancing by distributing incoming requests across all running replicas.

Benefits include:

- Improved availability
- Better resource utilization
- High scalability
- Automatic traffic distribution

---

# 🌐 Networking

The deployment uses Docker Swarm's **Overlay Network**, allowing services on different nodes to communicate securely.

Features include:

- Automatic service discovery
- Internal DNS
- Cross-node communication
- Secure networking

---

# 💥 Fault Tolerance Testing

To verify high availability, a worker node was intentionally stopped.

Observed results:

- ✅ Failed containers were automatically recreated
- ✅ Running services remained available
- ✅ Swarm rescheduled tasks on healthy nodes
- ✅ No manual intervention was required

This demonstrates Docker Swarm's built-in self-healing capabilities.

---

# 📸 Screenshots

Add screenshots inside a `screenshots/` folder.

Suggested screenshots:

- 🐳 Docker Image Build
- 📦 Running Container
- ☸️ Swarm Initialization
- 🖥️ Manager & Worker Nodes
- 📈 Service Scaling
- 🌐 Overlay Network
- 💥 Node Failure Simulation
- 📊 Running Containers

Example:

```markdown
![Docker Build](screenshots/docker-build.png)

![Swarm Nodes](screenshots/swarm-nodes.png)

![Scaling](screenshots/scaling.png)
```

---

# 📚 Learning Outcomes

This project demonstrates:

- ✅ Docker Fundamentals
- ✅ Image Creation
- ✅ Container Lifecycle
- ✅ Docker Compose
- ✅ Docker Swarm
- ✅ Cluster Management
- ✅ Service Deployment
- ✅ Load Balancing
- ✅ Horizontal Scaling
- ✅ High Availability
- ✅ Fault Tolerance
- ✅ Container Networking

---

# 🔮 Future Improvements

- ☸️ Kubernetes Deployment
- 🐳 Docker Registry Integration
- 🚀 GitHub Actions CI/CD
- 📊 Prometheus Monitoring
- 📈 Grafana Dashboard
- 🔍 ELK Logging Stack
- ☁️ Cloud Deployment (AWS/Azure/GCP)
- 🔐 Secrets Management

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

Feel free to fork the repository and submit a pull request.

---

# 📜 License

This project is licensed under the **MIT License**.

---

# ⭐ Support

If you found this project useful, please consider giving it a ⭐ on GitHub.

Happy Containerizing! 🐳🚀
