# [Mysql](https://hub.docker.com/_/mysql) 

| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | mysql |
| [IMAGE_TAG] | 9.5.0 or latest |
| [CONTAINER_NAME] | CONTAINER_NAME |
| [HOST_PORT] | HOST_PORT|
| [HOST_VOLUMN] | HOST_VOLUMN|
| [MYSQL_DATABASE] | MYSQL_DATABASE |
| [MYSQL_USER] | MYSQL_USER |
| [MYSQL_PASSWORD] | MYSQL_PASSWORD |

Usage :

```bash
docker run -d \
-p [HOST_PORT]:3306 \
-v [HOST_VOLUMN]:/var/lib/mysql \
-e MYSQL_DATABASE=[MYSQL_DATABASE] \
-e MYSQL_USER=[MYSQL_USER] \
-e MYSQL_PASSWORD=[MYSQL_PASSWORD] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 
```bash
docker run -d \
-p 3306:3306 \
-e MYSQL_DATABASE=guest \
-e MYSQL_USER=guest \
-e MYSQL_PASSWORD=guest \
--name guest-mysql \
mysql:9.5.0
```


# Packages

## Build
```bash
docker build --platform linux/arm64,linux/amd64 -t ghcr.io/u2waremanager/io.u2ware.examples.env.mysql:9.5.0 .
```


## Push
```bash
docker push ghcr.io/u2waremanager/io.u2ware.examples.env.mysql:9.5.0
```

# Pull
```bash
docker pull ghcr.io/u2waremanager/io.u2ware.examples.env.mysql:9.5.0
```

