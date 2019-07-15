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

Stop Minikube

```
minikube stop
```