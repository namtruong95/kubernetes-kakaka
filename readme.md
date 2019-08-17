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

## redis cache

```
docker build -t redis:latest api/caches/redis
```

# created pod

## Pod Postgres

```
kubectl create -f api/databases/postgres.yaml
```

## Pod Postgres

```
kubectl create -f api/caches/redis.yaml
```

# Created Service

## Service LB postgres

```
kubectl create -f services/postgres-lb.yaml
```

## Service LB redis

```
kubectl create -f services/redis-lb.yaml
```

# Created Volumes

## postgres volumes

```
kubectl create -f volumes/postgres-database-claim.yaml
```

## redis volumes

```
kubectl create -f volumes/redis-database-claim.yaml
```
