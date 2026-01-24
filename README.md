# User Data Entry Application (Spring Boot + MongoDB)

A simple **User Data Entry web application** built using **Spring Boot** and **MongoDB**, fully containerized using **Docker** and orchestrated with **Docker Compose**.

This project demonstrates how to:

* Build Docker images manually using a **Dockerfile**
* Run multi-container applications using **Docker Compose**
* Connect a Spring Boot application with MongoDB in a containerized environment

---

## 🚀 Tech Stack

* **Backend**: Spring Boot (Java)
* **Database**: MongoDB
* **Containerization**: Docker
* **Orchestration**: Docker Compose
* **Build Tool**: Maven

---

## 📌 Project Overview

This application allows users to:

* Enter user details through a web interface
* Store user data in MongoDB
* Retrieve and display stored user information

The entire application runs inside Docker containers, ensuring:

* Environment consistency
* Easy setup
* Platform independence

---

## 🧱 Architecture

```
User Browser
     │
     ▼
Spring Boot Application (Container)
     │
     ▼
MongoDB (Container)
```

* Spring Boot communicates with MongoDB using a Docker network
* MongoDB data is persisted using Docker volumes

---

## 📂 Project Structure

```
project-root/
│
├── Dockerfile
├── docker-compose.yml
├── pom.xml
├── src/
│   └── main/
│       ├── java/
│       └── resources/
│
└── README.md
```

---

## 🐳 Docker Implementation

### 1️⃣ Dockerfile

* Created manually to build the Spring Boot application image
* Uses a lightweight base image
* Packages the Spring Boot JAR inside the container

### 2️⃣ Docker Compose

* Manages multiple containers
* Starts both **Spring Boot** and **MongoDB** services
* Handles networking between containers
* Uses volumes for MongoDB data persistence

---

## ▶️ How to Run the Project

### Prerequisites

* Docker
* Docker Compose
* Git

---

### Step 1: Clone the Repository

```
git clone <repository-url>
cd <project-folder>
```

---

### Step 2: Build Docker Image Manually

```
docker build -t user-data-app .
```

---

### Step 3: Start Containers Using Docker Compose

```
docker-compose up -d
```

---

### Step 4: Access the Application

* Application URL: `http://localhost:8080`
* MongoDB runs internally inside Docker network

---

## 💾 Data Persistence

* MongoDB uses Docker volumes
* Data remains safe even if containers restart

---

## 🧪 Testing the Application

* Enter user details through UI or API
* Verify data is stored in MongoDB
* Restart containers to confirm data persistence

---

## 🎯 Key Learnings

* Dockerizing Spring Boot applications
* Multi-container setup using Docker Compose
* Service-to-service communication in Docker
* MongoDB persistence using volumes

---

## 📌 Future Enhancements

* Kubernetes deployment
* CI/CD integration using Jenkins
* Security enhancements
* Validation and exception handling

---

## 👤 Author

**Nitheesh Kumar Bellamkonda**
DevOps Engineer | Docker | Kubernetes | CI/CD | AWS 
---

## 📄 License

This project is for learning and demonstration purposes.
