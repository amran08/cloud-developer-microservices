## cloud-developer-microservices

## Github link:

https://github.com/amran08/cloud-developer-microservices

## Dockerhub Link:

https://hub.docker.com/u/amran08
https://hub.docker.com/r/amran08/udacity-frontend
https://hub.docker.com/r/amran08/udacity-reverse-proxy 
https://hub.docker.com/r/amran08/udacity-restapi-feed 
https://hub.docker.com/r/amran08/udacity-restapi-user


## Kubernetes Deployment

Created Kubernetes cluster using minikube

minikube start --cpu=4 --memory=8192

## Create Your own secret and config file

```
mv udacity-c3-deployment/k8s/samples/aws-secret-sample.yaml udacity-c3-deployment/k8s/aws-secret.yaml
mv udacity-c3-deployment/k8s/samples/env-secret-sample.yaml udacity-c3-deployment/k8s/env-secret.yaml
mv udacity-c3-deployment/k8s/samples/env-configmap-sample.yaml udacity-c3-deployment/k8s/env-configmap.yaml

```

##for Deploy application using services and deployment

kubectl apply -f udacity-c3-deployment/k8s

Check Cluster status

kubectl get all

Expose frontend and reverse proxy through port forward

    kubectl port-forward service/reverseproxy 8080:8080
    kubectl port-forward service/frontend 8100:8100

