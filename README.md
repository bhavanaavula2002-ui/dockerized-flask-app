# Dockerized Flask App

## Project Overview

This project is a simple Flask web application containerized using Docker. The purpose of this project is to learn Flask application setup, Docker containerization, Git and GitHub workflow, and troubleshooting common Git and Docker issues.

---

# Technologies Used

- Python
- Flask
- Docker
- Git
- GitHub
- HTML

---

# Project Structure

```bash
dockerized-flask-app/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── .gitignore
└── templates/
    └── index.html
```

---

# Step-by-Step Process

## 1. Created Project Folder

Commands used:

```bash
mkdir dockerized-flask-app
cd dockerized-flask-app
```

---

## 2. Initialized Git Repository

Command used:

```bash
git init
```

This created a local Git repository.

---

## 3. Created Flask Application

Created the following files:

- app.py
- requirements.txt
- templates/index.html

Tested the Flask app locally using:

```bash
python app.py
```

Output:

```bash
Running on http://127.0.0.1:5000
```

---

# Docker Setup

## 4. Created Dockerfile

Created a Dockerfile to containerize the Flask application.

---

## 5. Built Docker Image

Command used:

```bash
docker build -t flask-app .
```

Docker successfully built the image.

---

## 6. Ran Docker Container

Command used:

```bash
docker run -p 5000:5000 flask-app
```

Application successfully ran inside the Docker container.

---

# GitHub Setup

## 7. Connected Local Repository to GitHub

Command used:

```bash
git remote add origin https://github.com/bhavanaavula2002-ui/dockerized-flask-app.git
```

---

## 8. Renamed Branch to Main

Command used:

```bash
git branch -m main
```

---

# Problems Faced and Solutions

## Problem 1: src refspec main does not match any

Error:

```bash
error: src refspec main does not match any
```

### Reason

There were no commits in the repository.

### Solution

Added files and created the first commit:

```bash
git add .
git commit -m "Dockerized Flask app initial commit"
```

---

## Problem 2: Empty Folder Issue

When running:

```bash
dir
```

the folder showed:

```bash
0 File(s)
```

### Reason

Files were created in a different directory:

```bash
Desktop/dockerized-flask-app
```

### Solution

Moved to the correct folder:

```bash
cd Desktop\dockerized-flask-app
```

---

## Problem 3: Git Tracking Entire User Directory

Warnings:

```bash
warning: could not open directory 'Application Data/'
```

and many system folders appeared in `git status`.

### Reason

Git repository was accidentally initialized in:

```bash
C:\Users\avula
```

instead of the project folder.

### Solution

Checked Git root directory:

```bash
git rev-parse --show-toplevel
```

Output:

```bash
C:/Users/avula
```

Removed incorrect Git repository:

```bash
rmdir /s /q .git
```

Reinitialized Git inside the correct project folder:

```bash
cd Desktop\dockerized-flask-app
git init
```

---

## Problem 4: The system cannot find the path specified

Error:

```bash
cd Desktop\dockerized-flask-app
The system cannot find the path specified.
```

### Reason

Already inside the project directory.

### Solution

Used:

```bash
cd ..
```

or checked current directory using:

```bash
cd
```

---

# Final Successful Push to GitHub

Commands used:

```bash
git add .
git commit -m "Dockerized Flask app initial commit"
git remote add origin https://github.com/bhavanaavula2002-ui/dockerized-flask-app.git
git branch -m main
git push -u origin main
```

GitHub push completed successfully.

---

# How to Run the Project Locally

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Run Flask Application

```bash
python app.py
```

Open browser:

```bash
http://127.0.0.1:5000
```

---

# How to Run Using Docker

## Build Docker Image

```bash
docker build -t flask-app .
```

## Run Docker Container

```bash
docker run -p 5000:5000 flask-app
```

Open browser:

```bash
http://localhost:5000
```

---

# What I Learned

Through this project, I learned:

- How Git repositories work
- Difference between local and remote repositories
- Docker image creation
- Running applications in containers
- Debugging Git errors
- Managing project directories properly
- Pushing code to GitHub successfully

---
