# Minikube
- minikube start
- minikube status
- minikube kubectl -- version --client
- minikube kubectl get all

Add aliases for kubectl 
 * alias kubectl="minikube kubectl --"
 
- kubectl get pods
- kubectl get deployment
- kubectl get services
- kubectl get namespaces
- kubectl delete all --all  ---> warnings on delete all on production
---
### nginx exmaple
- kubectl create deployment nginx --image=nginx
- kubectl get all -o wide
- kubectl  describe deployment nginx
- kubectl  describe pod nginx-77b4fdf86c
- kubectl logs nginx-77b4fdf86c-sx9pq
- kubectl exec -it nginx-77b4fdf86c-sx9pq
  -- /bin/bash
- kubectl  edit deployment
- kubectl get all
- kubectl delete deployment nginx
- kubectl get all
-----
## K8 demo 
#### k8s-demo folder
- kubectl create namespace my-namespace
- cd k8s-demo/
- kubectl apply -f ./deploy.yaml -n my-namespace
- kubectl apply -f ./svc.yaml -n my-namespace
- kubectl get all -n my-namespace
### after we can delete 
- kubectl delete -f ./deploy.yaml
- kubectl delete -f ./svc.yaml
- kubectl get all
- ---
## Ingress service
- minikube addons list
- minikube addons enable ingress 
----

# Deploying Resources in K8s Cluster
- kubectl get all 
- minikube dashboard
- kubectl apply -f ./k8s/

- kubectl get services
- minikube service eureka-lb 
- minikube service cloud-gateway-svc
- kubectl delete -f ./k8s/