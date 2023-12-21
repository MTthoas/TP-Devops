# TP Devops

## Prerequis
minkikupe

## Step

minikupe start
kubectl create namespace frontend
kubectl create namespace backend
kubectl create namespace monitoring
kubectl create namespace postgresql

docker build -t mtthoas/app-frontend ./frontend
docker build -t mtthoas/app-backend ./api      
docker build -t mtthoas/database ./api      

kubectl run frontend --image=mtthoas/app-frontend --image-pull-policy=Never
kubectl run backend --image=mtthoas/app-backend --image-pull-policy=Never
kubectl run database --image=mtthoas/database --image-pull-policy=Never

kubectl port-forward prometheus-deployment-5549c769cc-j5h9d 8080:9090 -n monitoring


Minikupe 
<img width="1282" alt="Capture d’écran 2023-12-21 à 15 32 35" src="https://github.com/MTthoas/TP-Devops/assets/92540288/b80f27c6-f9fa-464c-9e70-f0c39ee86574">

Grafana & Prometheus 
<img width="1440" alt="Capture d’écran 2023-12-21 à 15 34 45" src="https://github.com/MTthoas/TP-Devops/assets/92540288/91d725b9-e5de-40b6-bcbe-37a2a8acc56a">

Alert Manager
<img width="1440" alt="Capture d’écran 2023-12-21 à 15 34 57" src="https://github.com/MTthoas/TP-Devops/assets/92540288/0a2f153f-d5e4-4d5b-aaf7-3c3009fd2da8">



