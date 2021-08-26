# Kafka for Kubernetes

It depends on [strimzi kafka](https://strimzi.io/) operator, why does it use strimzi kafka operator directly?
* strimzi kafka operator force to enable tls for zookeeper and kafka.
* strimzi operator just want to zookeeper serves kafka only, it denies pods requests expect kafka and zookeeper.
* Deploy too many components if you just want to deploy kafka and zookeeper soon.

## Quick start
```shell
https://github.com/qiffang/kubernetes-kafka.git
cd kubernetes-kafka
helm install kafka -n test kafka/
```

## Build images

> The base image is from strimiz kafka image, but we need to override tls and health check related files.

```shell
cd docker
docker build -t $image .
```