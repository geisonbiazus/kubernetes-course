Start Minikube

```
minikube start
```

Run image on kubernetes

```
kubectl run hello-minikube --image=gcr.io/google_containers/echoserver:1.8 --port=8080
```

Expose service port

```
kubectl expose deployment hello-minikube --type=NodePort
```

Get service URL

```
minikube service hello-minikube --url
```

Get service info

```
kubectl get service hello-minikube
```

Stop Minikube

```
minikube stop
```

List pods

```
kubectl get pods
```

List ndoes

```
kubectl get nodes
```

See all contexts

```
kubectl config get-contexts
```

select a context

```
kubectl config use-context minikube
```

Create a resource

```
kubectl create -f resourse_file.yml
```

Apply changes to a running resource

```
kubectl apply -f resourse_file.yml
```