# K8s infrastructure
---

how to run:

```
minikube start --driver=docker --docker-opt dns=8.8.8.8

```
pull images:

```
docker pull bitnamilegacy/postgresql:16.1.0-debian-11-r15
docker pull bitnamilegacy/mongodb:7.0.3-debian-11-r1
docker pull bitnamilegacy/redis:7.2.4-debian-11-r2
docker pull bitnamilegacy/kafka:3.6.1-debian-11-r0

docker pull ghcr.io/marketplace-internship-project/payment-service:latest
docker pull ghcr.io/marketplace-internship-project/order-service:latest
docker pull ghcr.io/marketplace-internship-project/user-service:latest
docker pull ghcr.io/marketplace-internship-project/authentication-service:latest
docker pull ghcr.io/marketplace-internship-project/api-gateway:latest
```

then load them into minikube 
```

minikube image load bitnamilegacy/postgresql:16.1.0-debian-11-r15
minikube image load bitnamilegacy/mongodb:7.0.3-debian-11-r1
minikube image load bitnamilegacy/redis:7.2.4-debian-11-r2
minikube image load bitnamilegacy/kafka:3.6.1-debian-11-r0

minikube image load ghcr.io/marketplace-internship-project/payment-service:latest
minikube image load ghcr.io/marketplace-internship-project/order-service:latest
minikube image load ghcr.io/marketplace-internship-project/user-service:latest
minikube image load ghcr.io/marketplace-internship-project/authentication-service:latest
minikube image load ghcr.io/marketplace-internship-project/api-gateway:latest
```

Use this for proper chatt usage
```
helm dependency build

helm install marketplace .

kubectl get pods -w
```