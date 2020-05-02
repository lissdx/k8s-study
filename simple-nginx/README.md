#### 1. Create Deployment file.
A Deployment provides declarative updates for Pods and ReplicaSets.
file deployment-app.yaml

## Create configmap from `default.conf` with ngnix configuration.

```bash
kubectl create configmap app --from-file default.conf
```

## Create a secret with key and value

```bash
kubectl create secret generic app --from-literal=password=MyGREATPASSword
```

## Create deployment's copy of `app`

```bash
kubectl get deploy app -o yaml --export >appsecret.yaml
or 
kubectl get deploy ngnix-server-deployment -o yaml --export >appsecret.yaml
```