# AWS 

## Pre-requisites

1. Install kubectl
2. Install kops
3. Instqll python and pip
4. Install awscli
5. Create an AWS account
6. Create a IAM user with admin access
7. Create a bucket to store state
8. Create a hosted for your domain zone on Route53
9. Add the DNS for the hosted zone to your domain registration

## Configuring

 Configure aws with your created user tokens

```
aws configure
```

## Working with kops

Create cluser

```
kops create cluster --name=kubernetes.geisonbiazus.com --state=s3://kops-state-ad21 --zones=eu-central-1a --node-size=t2.micro --master-size=t2.micro --dns-zone=kubernetes.geisonbiazus.com
```

Configure the cluster (confirm creation)

```
kops update cluster --name kubernetes.geisonbiazus.com --yes --state=s3://kops-state-ad21
```

Delete cluster

```
kops delete cluster kubernetes.geisonbiazus.com --yes --state=s3://kops-state-ad21
```