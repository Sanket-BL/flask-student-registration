# Flask Student Registration DevOps Project

## 📌 Project Overview

This project demonstrates the development and deployment of a **Flask-based Student Registration Web Application** using modern **DevOps practices**.

The application allows users to register student details through a web form. The submitted data is stored in a **MariaDB database** and displayed in a tabular format.

The project also demonstrates how a web application can be **containerized and deployed using Docker and automated using Jenkins CI/CD pipeline** on an **AWS EC2 instance**.

This project is designed to showcase practical skills in:

* Web Application Development
* DevOps CI/CD Automation
* Containerization
* Cloud Deployment
* Linux Server Management

---

# 🏗️ Architecture

Application Architecture:

User Browser
⬇
Flask Web Application
⬇
MariaDB Database
⬇
AWS EC2 Instance

CI/CD Pipeline:

Developer → GitHub → Jenkins Pipeline → Docker Build → Container Deployment → AWS EC2

---

# 🛠️ Technologies Used

### Backend

* Python
* Flask Framework

### Frontend

* HTML
* CSS

### Database

* MariaDB / MySQL

### DevOps Tools

* Docker
* Jenkins
* Git
* GitHub

### Cloud Platform

* Amazon Web Services (AWS EC2)

### Operating System

* Linux (Amazon Linux)

---

# 🚀 Features

* Student Registration Form
* Store student data in database
* Display registered students
* Containerized application using Docker
* Automated CI/CD pipeline using Jenkins
* Cloud deployment on AWS EC2 instance

---

# 📁 Project Structure

```
flask-student-registration
│
├── app.py
├── requirements.txt
├── Dockerfile
├── Jenkinsfile
├── README.md
│
├── templates
│   ├── register.html
│   └── students.html
│
└── static
    └── style.css
```

---

# 🗄️ Database Schema

Database: **studentdb**

Table: **students**

| Column  | Type    | Description     |
| ------- | ------- | --------------- |
| id      | INT     | Primary Key     |
| name    | VARCHAR | Student Name    |
| email   | VARCHAR | Student Email   |
| phone   | VARCHAR | Contact Number  |
| course  | VARCHAR | Course Name     |
| address | TEXT    | Student Address |

SQL Setup:

```
CREATE DATABASE studentdb;

USE studentdb;

CREATE TABLE students (
id INT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(100),
email VARCHAR(100),
phone VARCHAR(20),
course VARCHAR(100),
address TEXT
);
```

---

# ⚙️ Setup Instructions

## 1️⃣ Clone Repository

```
git clone https://github.com/Sanket-BL/flask-student-registration.git
cd flask-student-registration
```

---

## 2️⃣ Install Dependencies

```
pip install -r requirements.txt
```

---

## 3️⃣ Install Database

```
sudo yum install mariadb105-server -y
sudo systemctl start mariadb
```

Login to database:

```
sudo mysql
```

Create database and table.

---

## 4️⃣ Run Application

```
python3 app.py
```

Open browser:

```
http://EC2_PUBLIC_IP:5000
```

---

# 🐳 Docker Deployment

Build Docker Image:

```
docker build -t flask-student-app .
```

Run Docker Container:

```
docker run -d -p 5000:5000 flask-student-app
```

Verify container:

```
docker ps
```

---

# 🔄 Jenkins CI/CD Pipeline

The Jenkins pipeline automates the deployment process.

Pipeline stages:

1. Clone GitHub repository
2. Build Docker image
3. Deploy Docker container

Example CI/CD workflow:

GitHub → Jenkins → Docker Build → Container Deployment → AWS EC2

---

# ☁️ AWS Deployment

The application is deployed on an **AWS EC2 instance**.

Steps performed:

* Launch EC2 instance
* Install Docker and Jenkins
* Configure MariaDB database
* Deploy Flask application
* Automate deployment using Jenkins pipeline

---

# 📸 Project Screenshots

Add screenshots of:

* AWS EC2 Instance Running
* Flask Student Registration Form
* Registered Students Page
* MariaDB Database Table
* Docker Container Running
* Jenkins CI/CD Pipeline
* GitHub Repository

---

# 🔮 Future Improvements

* Implement Docker Compose
* Add Nginx Reverse Proxy
* Enable HTTPS with SSL
* Deploy using Kubernetes
* Infrastructure automation using Terraform
* Monitoring with Prometheus & Grafana

---

# 👨‍💻 Author

**Sanket Survase**

Cloud & DevOps Enthusiast

Skills:

* Linux
* AWS
* Docker
* Jenkins
* Python
* GitHub
* CI/CD Automation

---

# ⭐ Conclusion

This project demonstrates how a web application can be developed and deployed using **modern DevOps tools and practices**, combining cloud infrastructure, containerization, and automated CI/CD pipelines.
