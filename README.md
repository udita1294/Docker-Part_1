# Docker Part 1 – Node.js Express App with Docker

This project demonstrates how to **containerize a simple Node.js Express application using Docker**.
The application returns a simple **"Hello World"** response and runs inside a Docker container.

---

## 📌 Project Overview

The goal of this project is to understand the basics of Docker:

* Creating a **Dockerfile**
* Building a **Docker image**
* Running the application inside a **Docker container**

---

## 📂 Project Structure

```
Docker-Part_1
│
└── Backend
    │
    ├── Dockerfile
    ├── index.js
    ├── package.json
    ├── package-lock.json
    ├── .dockerignore
    └── .gitignore
```

---

## ⚙️ Technologies Used

* Node.js
* Express.js
* Docker

---

### Instructions Explained

| Command                 | Purpose                                 |
| ----------------------- | --------------------------------------- |
| FROM node:22-alpine     | Uses lightweight Node.js base image     |
| WORKDIR /app            | Sets working directory inside container |
| COPY . .                | Copies project files into container     |
| RUN npm install         | Installs dependencies                   |
| EXPOSE 3000             | Opens port 3000                         |
| CMD ["node","index.js"] | Starts the server                       |

---

```

### 3️⃣ Build Docker Image

```bash
docker build -t node-docker-app .
```

### 4️⃣ Run Docker Container

```bash
docker run -p 3000:3000 hello-world-app
```

---

## 🌐 Access the Application

Open your browser and visit:

```
http://localhost:3000
```

You should see:

```
Hello World
```

---

## 📖 What I Learned

* Basics of **Docker containers**
* Writing a **Dockerfile**
* Building Docker images
* Running Node.js apps inside Docker

