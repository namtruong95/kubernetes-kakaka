# using docker env to minikube

```
eval $(minikube -p kakaka docker-env)
```

# create a new cluster

```
minikube start -p kakaka --disk-size 100g --memory 4096
```
