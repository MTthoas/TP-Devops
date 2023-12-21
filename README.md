# TP Devops

## Prerequis
minikube

### Services
- /api : GO - Fiber
- /frontend : React
- /postgres : PostgreSQL

## Contribution
matthias pecquery 4IBC

## Step

```bash 
minikupe start
```
```bash 
kubectl create namespace frontend
```
```bash 
kubectl create namespace backend
```
```bash
kubectl create namespace monitoring
```
```bash 
kubectl create namespace postgresql
```

```bash 
docker build -t mtthoas/app-frontend ./frontend
```
```
bash docker build -t mtthoas/app-backend ./api
``` 
```
bash docker build -t mtthoas/database ./api
```  

```bash 
kubectl run frontend --image=mtthoas/app-frontend --image-pull-policy=Never
```
```bash 
kubectl run backend --image=mtthoas/app-backend --image-pull-policy=Never
```
```bash 
kubectl run database --image=mtthoas/database --image-pull-policy=Never
```

```bash 
kubectl port-forward prometheus-deployment-5549c769cc-j5h9d 8080:9090 -n monitoring
```

Minikube Dashboard
<img width="1282" alt="Capture d’écran 2023-12-21 à 15 32 35" src="https://github.com/MTthoas/TP-Devops/assets/92540288/b80f27c6-f9fa-464c-9e70-f0c39ee86574">

SonarCube
<img width="1534" alt="Capture d’écran 2023-12-21 à 15 39 33" src="https://github.com/MTthoas/TP-Devops/assets/92540288/2916c98a-1d8a-4d8d-b14f-4cea1c6f2f48">

Grafana & Prometheus 
<img width="1440" alt="Capture d’écran 2023-12-21 à 15 34 45" src="https://github.com/MTthoas/TP-Devops/assets/92540288/91d725b9-e5de-40b6-bcbe-37a2a8acc56a">

Alert Manager
<img width="1440" alt="Capture d’écran 2023-12-21 à 15 34 57" src="https://github.com/MTthoas/TP-Devops/assets/92540288/0a2f153f-d5e4-4d5b-aaf7-3c3009fd2da8">



