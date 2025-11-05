
# [Working with the Container registry](https://docs.github.com/ko/packages/working-with-a-github-packages-registry/working-with-the-container-registry)  

| Keyword | Description |
| --- | --- | 
| [PRODUCT] | postgres, rabbitmq, ....|
| [IMAGE_NAME] | 이미지 이름|
| [IMAGE_TAG] | 이미지 태그 또는 버전. latest|
| [USER_NAME] | 계정 이름 |
| [USER_TOKEN] | 계정 토큰 |
| [NAMESPACE] | 개인 계정 또는 조직의 이름 |


# Authentication

```bash
docker login ghcr.io -u [USER_NAME]
    Password: [USER_TOKEN]
    Login Succeeded
```

or 

```bash
export GITHUB_USER=[USER_NAME]
export GITHUB_TOKEN=[USER_TOKEN]

echo $GITHUB_USER
echo $GITHUB_TOKEN

docker login ghcr.io
```



# Build
```bash
cd [PRODUCT]
docker build -t [IMAGE_NAME]:[IMAGE_TAG] .
```


# Push (Publishing)
```bash
docker push ghcr.io/[NAMESPACE]/[IMAGE_NAME]:[IMAGE_TAG]
```


# Remove
```bash
docker rmi ghcr.io/[NAMESPACE]/[IMAGE_NAME]:[IMAGE_TAG]
```


# Pull (Installing)
```bash
docker pull ghcr.io/[NAMESPACE]/[IMAGE_NAME]:[IMAGE_TAG]
```




