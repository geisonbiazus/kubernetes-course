Describe replica controller

```
kubectl describe replicationcontroller helloworld-controller
kubectl describe rc 
```

Scale

```
kubectl scale --replicas=4 -f filename
kubectl scale --replicas=4 rc/helloworld-controller
```

Delete replica controller

```
kubectl delete rc/helloworld-controller
```