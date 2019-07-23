# Deployments

Run deployment 

```
kubectl create -c helloworld.yml
```

Expose port

```
kubectl expose deployment helloworld-deployment --type=NodePort
minikube service helloworld-deployment --url
```

Get information on current deployment

```
kubectl get deployments
```

Get information about the replica sets

```
kubectl get rs
```

get pods, and als show labels

```
kubectl get pods --show-labels
```

Get deployment status

```
kubectl rollout status deployment/helloworld-deployment
```

Run another image on deployment

```
kubectl set image deployment/helloworld-deployment k8s-demo=k8s-demo:2
```

Edit deployment object

```
kubectl edit deployment/helloworld-deployment
```

Get the rollout history

```
kubectl rollout history deployment/helloworld-deployment
```

Rollback the rollout history (optional --to-revision=n)

```
kubectl rollout undo deployment/helloworld-deployment 
```
