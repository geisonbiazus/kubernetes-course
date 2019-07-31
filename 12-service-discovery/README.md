## Tesing resolve

Open a busybox image

```
kubectl run -i --tty busybox --image=busybox --restart=Never -- sh
```

Search for the service

```
nslookup helloworld-db-service
```