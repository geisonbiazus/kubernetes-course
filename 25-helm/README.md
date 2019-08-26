# Helm

## Install helm
```
wget https://storage.googleapis.com/kubernetes-helm/helm-v2.11.0-linux-amd64.tar.gz
tar -xzvf helm-v2.11.0-linux-amd64.tar.gz
sudo mv linux-amd64/helm /usr/local/bin/helm
```

## Initialize helm

```
kubectl create -f helm-rbac.yaml
helm init --service-account tiller
```

## Create a chart

```
helm create mychart
```
## Deploy a chart

```
helm install mychart/
```


## Node demo app Chart

### Download dependencies
```
helm dependency update
```

### Install Chart
```
helm install .
```

### Upgrade Chart
```
helm upgrade --set image.tag=v0.0.2,mariadb.db.password=$DB_APP_PASS RELEASE .
```

## List Releases
```
helm history NAME
```

## Rollback
```
helm rollback NAME REVISION
```

## Setup S3 helm repository
Make sure to set the default region in setup-s3-helm-repo.sh
```
./setup-s3-helm-repo.sh
```

## Package and push demo-chart

```
export AWS_REGION=yourregion # if not set in ~/.aws
helm package demo-chart
helm s3 push ./demo-chart-0.0.1.tgz my-charts
```
