# 1. Build Image

> docker build -t ros_humble:aptgetter .


# 2. Run

> {my_ros#1} docker run \
    --rm -it \
    --name my_ros \
    ros_humble:aptgetter \
    bash

                                                -e DISPLAY="host.docker.internal:0" \
                                                --privileged  \
                                                --hostname $(hostname) \
                                                --network host \
                                                --env="QT_X11_NO_MITSHM=1" \
                                                -v /tmp/.X11-unix:/tmp/.X11-unix:ro \


> {my_ros#2} docker exec -it my_ros /bin/bash

> {my_ros#1} echo $ROS_DISTRO
> {my_ros#2} echo $ROS_DISTRO

> {my_ros#1} ros2 run demo_nodes_cpp talker
> {my_ros#2} ros2 run demo_nodes_py listener

> {my_ros#1} ros2 run turtlesim turtlesim_node
> {my_ros#2} ros2 run turtlesim turtle_teleop_key


