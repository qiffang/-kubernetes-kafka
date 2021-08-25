# Kafka for Kubernetes

It depends on strimiz kafka operator, but it is more convenient
* Disable tls for zookeeper and kafka
* Modifying the configuration is easier

## Quick start
```shell
helm install kafka -n test kafka/
```

## Build images

> The base image is from strimiz kafka image, but we need to override tls related files.

```shell
cd docker
docker build -t $image .
```