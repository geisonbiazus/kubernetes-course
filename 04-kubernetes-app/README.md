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

Describe service

```
kubectl describe service nodehelloworld-service
```

Attach to a container

```
kubectl attach nodehelloworld.example.com
```

Execute a command

```
kubectl exec nodehelloworld.example.com ls /app
```

Execute a shell in a new pod with the busybox image

```
kubectl run -i --tty busybox --image=busybox --restart=Never -- sh
```

Get pod info and show container statuses

```
kubectl get pod helloworld-deployment-d66889848-fgq9w -o yaml
```