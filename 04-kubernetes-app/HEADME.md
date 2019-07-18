Create a pod

```
kubectl create -f helloworld.yml
```

Get pod information

```
kubectl describe pod nodehelloworld.example.com
```

Port forward

```
kubectl port-forward nodehelloworld.example.com 8081:3000
```

Expose port (create service)

```
kubectl expose pod nodehelloworld.example.com --type=NodePort --name=nodehelloworld-service
```

Get the cluser ip address. You can use the ip address of the master node

```
minikube service nodehelloworld-service --url
```