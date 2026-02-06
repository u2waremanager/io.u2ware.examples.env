# [MSSQL Server](https://learn.microsoft.com/ko-kr/sql/linux/quickstart-install-connect-docker?view=sql-server-ver17&tabs=cli&pivots=cs1-bash) 

| Keyword | Description |
| --- | --- | 
| [IMAGE_NAME] | mcr.microsoft.com/mssql/server |
| [IMAGE_TAG] | 2025-latest |
| [CONTAINER_NAME] | CONTAINER_NAME |
| [HOST_PORT] | HOST_PORT|
| [HOST_VOLUMN] | HOST_VOLUMN|


| [MSSQL_SA_PASSWORD] | MSSQL_SA_PASSWORD |

Usage :

```bash
docker run -d \
-p [HOST_PORT]:1433 \
-v [HOST_VOLUMN]:/var/opt/mssql/data \
-e MSSQL_SA_PASSWORD=[MSSQL_SA_PASSWORD] \
--name [CONTAINER_NAME] \
[IMAGE_NAME]:[IMAGE_TAG]
```

Example : 
```bash
docker run -d \
-p 1433:1433 \
-e MSSQL_SA_PASSWORD=guest \
--name guest-mssql \
mcr.microsoft.com/mssql/server:2025-latest 
```


# Packages

## Build
```bash
docker build --platform linux/arm64,linux/amd64 -t ghcr.io/u2waremanager/io.u2ware.examples.env.mssqlserver:2025-latest .
```


## Push
```bash
docker push ghcr.io/u2waremanager/io.u2ware.examples.env.mssqlserver:2025-latest
```

# Pull
```bash
docker pull ghcr.io/u2waremanager/io.u2ware.examples.env.mssqlserver:2025-latest
```

