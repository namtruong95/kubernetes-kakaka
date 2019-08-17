# using docker env to minikube

```
eval $(minikube -p kakaka docker-env)
```

# create a new cluster

```
minikube start -p kakaka --disk-size 100g --memory 4096
```

# build images

## postgres database

```
docker build -t postgres:latest api/databases/postgres
```

# created pod

## Pod Postgres

```
kubectl create -f api/databases/postgres.yaml
```
