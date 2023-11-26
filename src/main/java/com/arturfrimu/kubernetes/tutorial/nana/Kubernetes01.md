# Install on Mac os

[Kubernetes Tutorial for Beginners FULL COURSE in 4 Hours](https://www.youtube.com/watch?v=X48VuDVv0do)

```shell
brew install hyperkit
```

```shell
brew install minikube
```

```shell
kubectl
```

```shell
minikube
```

```shell
minikube start --vm-driver=hyperkit
```

```shell
kubectl get nodes
```

```shell
minikube status
```

```shell
kubectl version
```

```shell
kubectl get pod
```

```shell
kubectl get services
```

```shell
kubectl create -h
```

```shell
kubectl create deployment nginx-depl --image=nginx
```

```shell
kubectl get deployment
```

```shell
kubectl get pod
```

```shell
kubectl get replicaset
```

```shell
kubectl edit deployment nginx-depl
```

### Pod logs : `kubectl logs pod-name`
```shell
kubectl logs nginx-depl-6777bffb6f-s7n5j
```

```shell
kubectl create deployment mongo-depl --image=mongo
```

```shell
kubectl logs mongo-depl-558475c797-xtn9g
```

```shell
kubectl describe pod mongo-depl-558475c797-xtn9g
```

```shell
kubectl exec -it mongo-depl-558475c797-xtn9g -- bin/bash
```

### commands:
- ls
- exit

```shell
kubectl get deployment
```

```shell
kubectl delete deployment mongo-depl
```

```shell
kubectl get deployment
```

```shell
kubectl get pod
```

```shell
kubectl get replicaset
```

```shell
kubectl delete deployment nginx-depl
```

```shell
kubectl get deployment
```

```shell
kubectl get pod
```

```shell
kubectl get replicaset
```

### Create a file nginx-deployment.yaml with deployment configuration

```shell
kubectl apply -f nginx-deployment.yaml
```

```shell
kubectl get deployment
```

```shell
kubectl get pod
```

```shell
kubectl get replicaset
```

### Edit  nginx-deployment.yaml replicas to 2

```shell
kubectl apply -f nginx-deployment.yaml
```

```shell
kubectl get deployment
```

```shell
kubectl get pod
```

```shell
kubectl get replicaset
```

### Personal test. Delete 1 pod manually and look if K8s starts automatically a new pod
```shell
kubectl get pods
```

```shell
kubectl delete pod nginx-deployment-854bc88786-687qq
```

```shell
kubectl get pod
```

```shell
kubectl get deployment
```

```shell
kubectl get replicaset
```

### Create one deployment and one service

```shell
kubectl apply -f nginx-deployment.yaml
```

```shell
kubectl apply -f nginx-service.yaml
```

```shell
kubectl get pod
```

```shell
kubectl get services
```

```shell
kubectl describe services nginx-service
```

```shell
kubectl get pod -o wide
```

Poti vedea ca ip-urile podurilor coincid cu cele din Endpoints la service

### Status created by Kubernetes

```shell
kubectl get deployment nginx-deployment -o yaml
```

Poti compara nginx-deployment.yaml cu nginx-deployment-status-k8s.yaml sa vezi ce a adugat k8s la deployment dupa creare

### Delete deployment with file

```shell
kubectl delete -f nginx-deployment.yaml
```

### Delete service with file

```shell
kubectl delete -f nginx-service.yaml
```