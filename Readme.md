This is a simple application written in Golang to up and running in K8S.

build the docker image file:
```
docker build -t devops/goapp:1.0.0 .
```

apply configs:

create namespace and check that it's created:
```
kubectl apply -f k8s/namespace.yml
kubectl get namepsaces
```

```
kubectl apply -f k8s/deployment.yml
kubectl apply -f k8s/service.yml
kubectl apply -f k8s/ingress.yml
```

show running pods:
```
kubectl get pods --namespace=my-namespace
kubectl get services --namespace=my-namespace
kubectl get ingress -A
```

The appliction is accessable from ingress IP address.