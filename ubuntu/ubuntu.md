
# [udorowu/ubuntu-desktop-lxde-vnc](https://hub.docker.com/r/dorowu/ubuntu-desktop-lxde-vnc)
> docker run --rm -p 6080:80 -p 5900:5900 -v /dev/shm:/dev/shm dorowu/ubuntu-desktop-lxde-vnc


# [msjpq/wine-vnc](https://hub.docker.com/r/msjpq/wine-vnc)
> docker run --rm -p 8080:8080 -p 5900:5900 msjpq/wine-vnc:bionic



# [x11vnc/desktop](https://hub.docker.com/r/x11vnc/desktop) 
> docker run --rm -it -d -p 6080:80 -p 5901:5901 -p 5900:5900 x11vnc/desktop:20.04 


# ubuntu:22.04 Dockerfile

> docker pull ubuntu:22.04

> docker build -t my_ubuntu:aptgetter .

> docker run -d --name my_ubuntu my_ubuntu:aptgetter 

> docker exec -it my_ubuntu bash


# version
>> lsb_release -a
