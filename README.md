# 🚀 Docker & Git Setup with Spring Boot App Deployment

This guide provides step-by-step instructions to install Docker, Docker Compose, and Git on a Linux (Amazon Linux / CentOS) system, configure Git, and deploy a Spring Boot application using Docker and Docker Compose.

---

## 📌 Prerequisites
- Linux-based system (Amazon Linux, CentOS, RHEL, etc.)
- Sudo/root access

---

## ⚙️ Step 1: Update System
```bash
sudo yum update -y
```

---

## 🐳 Step 2: Install Docker
```bash
sudo yum install docker -y
docker --version
sudo systemctl start docker
sudo systemctl enable docker
```

---

## 🧩 Step 3: Install Docker Compose
```bash
sudo mkdir -p /usr/local/lib/docker/cli-plugins
sudo curl -SL https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-linux-x86_64 -o /usr/local/lib/docker/cli-plugins/docker-compose
sudo chmod +x /usr/local/lib/docker/cli-plugins/docker-compose
sudo docker compose version
```

---

## 🔑 Step 4: Docker Login
```bash
sudo docker login
```

---

## 📂 Step 5: Install Git & Configure
```bash
sudo yum install git -y
git --version
git config --global user.name "Saikiran Asamwar"
git config --global user.email "saikiranasamwar@gmail.com"
git config --list
```

---

## 📥 Step 6: Clone Spring Boot App
```bash
git clone https://github.com/atulkamble/docker-springboot-app.git
cd docker-springboot-app/
```

---

## 🛠 Step 7: Build & Push Docker Image
```bash
# Build image
sudo docker build -t saikiranasamwar4/docker-springboot-app .

# List images
sudo docker images

# Push image to Docker Hub
sudo docker push saikiranasamwar4/docker-springboot-app
```

---

## ▶️ Step 8: Run Docker Container
```bash
# Run on port 8080
sudo docker run -d -p 8080:8080 saikiranasamwar4/docker-springboot-app

# List running containers
sudo docker container ls

# Stop & remove a container
sudo docker container stop <container_id>
sudo docker container rm <container_id>
```

---

## 📦 Step 9: Run with Docker Compose
```bash
# Start in detached mode
sudo docker compose up -d

# Stop containers
sudo docker compose down
```

---

## 👨‍💻 Author

**Saikiran Rajesh Asamwar**  
Certified AWS DevOps Engineer

- 🌐 GitHub: [@SaikiranAsamwar](https://github.com/SaikiranAsamwar)
- 💼 LinkedIn: [Saikiran Asamwar](https://www.linkedin.com/in/saikiran-asamwar/)
- 📧 Email: saikiranasamwar@gmail.com

---tps://github.com/SaikiranAsamwar)  
- Email: saikiranasamwar@gmail.com  

---

