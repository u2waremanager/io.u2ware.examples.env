# Build Image
> docker build -t <IMAGE_NAME>:<IMAGE_TAG> .


> docker build -t postgres:u2ware .

# Push Image

> docker login ghcr.io -u <USER_NAME>
> docker login ghcr.io -u u2waremanager
Password:
Login Succeeded


> docker push ghcr.io/<NAMESPACE>/<IMAGE_NAME>:<IMAGE_TAG>


# Pull Image
> docker rmi ghcr.io/<NAMESPACE>/<IMAGE_NAME>:<IMAGE_TAG>




