docker build -t mtthoas/app-frontend ./frontend
docker build -t mtthoas/app-backend ./api      


kubectl run frontend --image=mtthoas/app-frontend --image-pull-policy=Never
kubectl run backend --image=mtthoas/app-backend --image-pull-policy=Never


<!-- ~/projects/eval/Dex main* ❯ kubectl create namespace backend
namespace/backend created

~/projects/eval/Dex main* ❯ kubectl create namespace frontend

minikube image load mtthoas/app-frontend:tag 
minikube image load mtthoas/app-backend:tag


docker push mtthoas/app-frontend:tag 
docker push mtthoas/app-backend:tag 


kubectl run first-container --image=first-image --image-pull-policy=Never --restart=Never

kubectl run backend --image=backend --image-pull-policy=Never --restart=Never -->


