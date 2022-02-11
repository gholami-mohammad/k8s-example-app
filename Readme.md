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
```

show running pods:
```
kubectl get pods --namespace=my-namespace
```