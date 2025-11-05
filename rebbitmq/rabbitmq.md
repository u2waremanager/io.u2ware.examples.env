# [RabbitMQ](https://hub.docker.com/_/rabbitmq) 

| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | 이미지 이름|
| [IMAGE_TAG] | 이미지 태그 또는 버전. latest|
| [CONTAINER_NAME] | CONTAINER_NAME |
| [RABBITMQ_DEFAULT_USER] | POSTGRES_USER |
| [RABBITMQ_DEFAULT_PASS] | POSTGRES_PASSWORD |


# Build 
Usage : 

```bash
docker build -t [IMAGE_NAME]:[IMAGE_TAG] .
```

Example : 
> docker build -t rabbitmq:3-management .


# Run 
Usage :

```bash
docker run -d \
-p 15672:15672 \
-p 5672:5672 \
-p 61613:61613 \
-e RABBITMQ_DEFAULT_USER=[RABBITMQ_DEFAULT_USER] \
-e RABBITMQ_DEFAULT_PASS=[RABBITMQ_DEFAULT_PASS] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 

> docker run -d \
    -p 15672:15672 \
    -p 5672:5672 \
    -p 61613:61613 \
    -e RABBITMQ_DEFAULT_USER=guest \
    -e RABBITMQ_DEFAULT_PASS=guest \
    --name yours-rabbitmq \
    rabbitmq:3-management