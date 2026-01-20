# [Postgres](https://hub.docker.com/_/postgres) 

| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | postgres|
| [IMAGE_TAG] | 16.4-alpine3.20 or latest|
| [CONTAINER_NAME] | guest-postgres |
| [HOST_PORT] | HOST_PORT|
| [HOST_VOLUMN] | HOST_VOLUMN|
| [POSTGRES_DB] | POSTGRES_DB |
| [POSTGRES_USER] | POSTGRES_USER |
| [POSTGRES_PASSWORD] | POSTGRES_PASSWORD |

Usage :

```bash
docker run -d \
-p [HOST_PORT]:5432 \
-v [HOST_VOLUMN]:/var/lib/postgresql/data \
-e POSTGRES_HOST_AUTH_METHOD=trust \
-e POSTGRES_DB=[POSTGRES_DB] \
-e POSTGRES_USER=[POSTGRES_USER] \
-e POSTGRES_PASSWORD=[POSTGRES_PASSWORD] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 
```bash
docker run -d \
-p 5432:5432 \
-e POSTGRES_HOST_AUTH_METHOD=trust \
-e POSTGRES_DB=guest \
-e POSTGRES_USER=guest \
-e POSTGRES_PASSWORD=guest \
--name guest-postgres \
postgres:16.4-alpine3.20
```


# Github Packages

## Build
```bash
docker build --platform linux/arm64,linux/amd64 -t ghcr.io/u2waremanager/io.u2ware.examples.env:postgres-16.4-alpine3.20 .
```
```bash
[IMAGE_NAME]: ghcr.io/u2waremanager/io.u2ware.examples.env
[IMAGE_TAG] : postgres-16.4-alpine3.20
```

## Push
```bash
docker push ghcr.io/u2waremanager/io.u2ware.examples.env:postgres-16.4-alpine3.20
```


# Pull
```bash
docker pull ghcr.io/u2waremanager/io.u2ware.examples.env:postgres-16.4-alpine3.20
```
