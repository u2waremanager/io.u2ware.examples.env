# [mariadb](https://hub.docker.com/_/mariadb) 

| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | mariadb |
| [IMAGE_TAG] | 10.11 or latest |
| [CONTAINER_NAME] | CONTAINER_NAME |
| [HOST_PORT] | HOST_PORT|
| [HOST_VOLUMN] | HOST_VOLUMN|
| [MARIADB_ROOT_PASSWORD] | MARIADB_ROOT_PASSWORD |
| [MARIADB_USER] | MARIADB_USER |
| [MARIADB_PASSWORD] | MARIADB_PASSWORD |
| [MARIADB_DATABASE] | MARIADB_DATABASE |

Usage :

```bash
docker run -d \
-p [HOST_PORT]:3306 \
-v [HOST_VOLUMN]:/var/lib/mysql:Z \
-e MARIADB_ROOT_PASSWORD=[MARIADB_ROOT_PASSWORD] \
-e MARIADB_USER=[MARIADB_USER] \
-e MARIADB_PASSWORD=[MARIADB_PASSWORD] \
-e MARIADB_DATABASE=[MARIADB_DATABASE] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 
```bash
docker run -d \
-p 3306:3306 \
-e MARIADB_ROOT_PASSWORD=guest \
-e MARIADB_USER=guest \
-e MARIADB_PASSWORD=guest \
-e MARIADB_DATABASE=guest \
--name guest-mariadb \
mariadb:10.11
```


# Packages

## Build
```bash
docker build --platform linux/arm64,linux/amd64 -t ghcr.io/u2waremanager/io.u2ware.examples.env.mariadb:10.11 .
```


## Push
```bash
docker push ghcr.io/u2waremanager/io.u2ware.examples.env.mariadb:10.11
```

# Pull
```bash
docker pull ghcr.io/u2waremanager/io.u2ware.examples.env.mariadb:10.11
```

