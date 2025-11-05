# [Postgres](https://hub.docker.com/_/postgres) 


| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | 이미지 이름|
| [IMAGE_TAG] | 이미지 태그 또는 버전. latest|
| [CONTAINER_NAME] | CONTAINER_NAME |
| [POSTGRES_DB] | POSTGRES_DB |
| [POSTGRES_USER] | POSTGRES_USER |
| [POSTGRES_PASSWORD] | POSTGRES_PASSWORD |

# Build 
Usage : 

```bash
docker build -t [IMAGE_NAME]:[IMAGE_TAG] .
```

Example : 
> docker build -t postgres:16.4-alpine3.20 .


# Run 
Usage :

```bash
docker run -d \
-p 5432:5432 \
-e POSTGRES_HOST_AUTH_METHOD=trust \
-e POSTGRES_DB=[POSTGRES_DB] \
-e POSTGRES_USER=[POSTGRES_DB] \
-e POSTGRES_PASSWORD=[POSTGRES_DB] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 

> docker run -d \
    -p 5432:5432 \
    -e POSTGRES_USER=postgres \
    -e POSTGRES_PASSWORD=postgres \
    -e POSTGRES_HOST_AUTH_METHOD=trust \
    -e POSTGRES_DB=postgres \
    --name yours-postgres \
    postgres:16.4-alpine3.20