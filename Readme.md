Understood, Sir — here is the entire DevOps Internals Revision Sheet for Ubuntu systems, covering Q1 to Q8 in the cleanest, fastest, exam-ready format.

This is exactly what you need for tomorrow.
Short. Perfect. No unnecessary lines.
Copy → Paste → Perform.


---

✅ Q1 — User Registration Form + Git Init + Push

index.html

<form>
  Name: <input type="text"><br>
  Email: <input type="email"><br>
  Phone: <input type="text"><br>
</form>

Git Commands

git init
git add .
git commit -m "Initial commit"
git remote add origin <your-repo-url>
git push -u origin main


---

✅ Q2 — Branch → Add Field → Merge → Push

Commands

git branch update-form
git checkout update-form

Add in HTML:

Department: <input type="text"><br>

Then:

git add .
git commit -m "Added department field"
git checkout main
git merge update-form
git push origin main


---

✅ Q3 — Jenkins CI Setup

Steps:

1. Open Jenkins → New Item → Freestyle Project


2. Source Code Management → Git → Add repo URL


3. Build Triggers → GitHub hook OR Poll SCM (* * * * *)


4. Build Step → Execute Shell



echo "Building project..."

5. Save → Build Now


6. Update HTML → commit & push → Jenkins auto builds.




---

✅ Q4 — Simple Web App + Dockerfile + Build + Run

index.html

<h1>Hello from Docker!</h1>

Dockerfile

FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html

Commands:

docker build -t mywebapp .
docker run -d -p 8080:80 --name mycontainer mywebapp
docker ps

Access:
👉 http://localhost:8080


---

✅ Q5 — Docker: List, Stop, Remove

Setup:

docker pull nginx
docker run -d -p 8080:80 --name mycontainer nginx

Commands:

docker ps
docker ps -a
docker images

docker stop mycontainer
docker rm mycontainer
docker rmi nginx


---

✅ Q6 — Kubernetes Deployment (Minimal YAML)

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

Commands:

kubectl apply -f deployment.yaml
kubectl get pods
kubectl get deployments

Pod must show Running.


---

✅ Q7 — NodePort Service + Access + Scale

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

Commands:

kubectl apply -f service.yaml
kubectl get svc

Get Node IP (Ubuntu):

minikube ip

Access:

http://<NODE-IP>:30080

Scale:

kubectl scale deployment mywebapp --replicas=3
kubectl get pods


---

✅ Q8 — ML Environment + requirements.txt + Notebook + Git

requirements.txt

numpy
pandas
scikit-learn
matplotlib

Install:

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter notebook

Notebook test cell:

import numpy as np
import pandas as pd
from sklearn.linear_model import LinearRegression
print("ML environment OK")

Git:

git add .
git commit -m "ML setup added"
git push


---

🎯 DONE — Your Complete Ubuntu Revision Pack

If you want, I can also make:
🔥 A single PDF-style final answer sheet
🔥 A one-page cheat-sheet
🔥 A viva-ready explanation for each question

Just tell me, Sir.