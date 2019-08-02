## Configmap as a file

Create the config map

```
kubectl create configmap nginx-config --from-file=13-configmap/reverseproxy.conf
```

See configmap value

```
kubectl get configmap nginx-config -o yaml
```

Run the pod and service

```
kubectl create -f 13-configmap/nginx.yml
kubectl create -f 13-configmap/nginx-service.yml
```

Get the URL

```
minikube service helloworld-nginx-service --url
```
