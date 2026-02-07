# [RabbitMQ](https://hub.docker.com/_/rabbitmq) 

| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | rabbitmq |
| [IMAGE_TAG] | 3-management or latest |
| [CONTAINER_NAME] | CONTAINER_NAME |
| [HOST_PORT_1] | HOST_PORT for AMQP |
| [HOST_PORT_2] | HOST_PORT for UI/UX |
| [HOST_PORT_3] | HOST_PORT for STOMP |
| [RABBITMQ_DEFAULT_USER] | POSTGRES_USER |
| [RABBITMQ_DEFAULT_PASS] | POSTGRES_PASSWORD |



### Usage :

```bash
docker run -d \
-p [HOST_PORT_1]:15672 \
-p [HOST_PORT_2]:5672 \
-p [HOST_PORT_3]:61613 \
-e RABBITMQ_DEFAULT_USER=[RABBITMQ_DEFAULT_USER] \
-e RABBITMQ_DEFAULT_PASS=[RABBITMQ_DEFAULT_PASS] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 
```bash
docker run -d \
-p 15672:15672 \
-p 5672:5672 \
-p 61613:61613 \
-e RABBITMQ_DEFAULT_USER=guest \
-e RABBITMQ_DEFAULT_PASS=guest \
--name guest-rabbitmq \
rabbitmq:3-management
```

# Package

### Build
```bash
docker build --platform linux/arm64,linux/amd64 -t ghcr.io/u2waremanager/io.u2ware.examples.env.rabbitmq:3-management .
```

### Push
```bash
docker push ghcr.io/u2waremanager/io.u2ware.examples.env.rabbitmq:3-management
```

### Pull
```bash
docker pull ghcr.io/u2waremanager/io.u2ware.examples.env.rabbitmq:3-management
```
