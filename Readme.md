Understood, Sir.
Here is the complete DevOps Internal Exam README containing ALL 8 PROGRAMS, each with:

Correct explanation

Full commands

Minimal working code

Clean formatting

Fully ready to submit or revise


Everything is in README.md format.


---

📘 README.md — DevOps Internal Programs (Q1–Q8)

(Copy–paste directly for your lab, perfect formatting)


---

# DevOps Internal Exam Programs — Complete README

This document contains all 8 programs with minimal working code, commands, and explanations.

---

# ✅ **Program 1: User Registration Form + Git Init + Push**

## **HTML File (registration.html)**
```html
<!DOCTYPE html>
<html>
<body>
  <h2>User Registration Form</h2>

  <form>
    Name: <input type="text"><br><br>
    Email: <input type="email"><br><br>
    Phone: <input type="text"><br><br>
    <button>Register</button>
  </form>

</body>
</html>

Git Commands

git init
git add .
git commit -m "Initial commit - user registration form"
git remote add origin <your-repo-url>
git push -u origin main


---

✅ Program 2: Branching, Editing, Merging

Create branch

git branch update-form
git checkout update-form

Add Department field

Department: <input type="text"><br><br>

Commit changes

git add .
git commit -m "Added department field"

Merge to main

git checkout main
git merge update-form
git push origin main


---

✅ Program 3: Jenkins CI Setup

Steps

1. Open Jenkins → New Item → Freestyle Project


2. SCM → Select Git → Add repo URL


3. Build Triggers →

Enable: GitHub hook trigger for GITScm polling

OR enable: Poll SCM → * * * * *



4. Build step → Execute Shell:



echo "Building Student Portal Website..."

5. Save → Build Now



Trigger CI

Make small change → push → Jenkins auto builds.


---

✅ Program 4: Docker Web Application

index.html

<h1>Hello from Docker!</h1>
<p>This application runs inside a Docker container.</p>

Dockerfile

FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html

Commands

docker build -t mywebapp .
docker run -d -p 8080:80 --name mycontainer mywebapp
docker ps


---

✅ Program 5: Docker Commands – List, Stop, Remove

Pull and run image

docker pull nginx
docker run -d -p 8080:80 --name mycontainer nginx

List containers & images

docker ps
docker ps -a
docker images

Stop container

docker stop mycontainer

Remove container

docker rm mycontainer

Remove image

docker rmi nginx


---

✅ Program 6: Kubernetes Deployment (Minimal YAML)

deployment.yaml

apiVersion: apps/v1
kind: Deployment
metadata:
  name: mywebapp
spec:
  selector:
    matchLabels:
      app: mywebapp
  template:
    metadata:
      labels:
        app: mywebapp
    spec:
      containers:
      - name: mywebapp
        image: mywebapp:latest

Commands

kubectl apply -f deployment.yaml
kubectl get pods
kubectl get deployments


---

✅ Program 7: NodePort Service + Access + Scaling

service.yaml

apiVersion: v1
kind: Service
metadata:
  name: mywebapp-service
spec:
  type: NodePort
  selector:
    app: mywebapp
  ports:
  - port: 80
    targetPort: 80
    nodePort: 30080

Commands

kubectl apply -f service.yaml
kubectl get svc

Get Node IP

minikube ip

Access app

http://<NODE-IP>:30080

Scale deployment

kubectl scale deployment mywebapp --replicas=3
kubectl get pods


---

✅ Program 8: ML Environment Setup + Jupyter Notebook + Git

requirements.txt

numpy
pandas
scikit-learn
matplotlib

Install environment

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook

Notebook test cell

import numpy as np
import pandas as pd
from sklearn.linear_model import LinearRegression
import matplotlib.pyplot as plt

print("ML environment successfully set up!")

Git Commit

git add .
git commit -m "Added ML environment setup and notebook"
git push origin main


---

🎉 COMPLETED — All DevOps Internal Programs Clean + Minimal + Correct

This README contains everything needed for your internal exam.

---

# ⭐ Sir, your README is fully ready.

If you want, I can:

✅ Export as **PDF**  
✅ Add **diagrams**  
✅ Add **viva answers**  
✅ Make an even more compact **cheat-sheet**  

Just tell me.