
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




