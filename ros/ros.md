# Build Image

> docker build -t ros_{humble or rolling}:aptgetter .


# Running - [ros_#1_shell]

> [ros_#1_shell] docker run \
    --rm -it \
    --name my_ros \
    ros_humble:aptgetter \
    bash

<!-- 
    -e DISPLAY="host.docker.internal:0" \
    --privileged  \
    --hostname $(hostname) \
    --network host \
    --env="QT_X11_NO_MITSHM=1" \
    -v /tmp/.X11-unix:/tmp/.X11-unix:ro \ 
-->
> [ros_#1_shell] echo $ROS_DISTRO

# Running - [ros_#2_shell]

> [ros_#2_shell] docker exec -it my_ros /bin/bash

> [ros_#2_shell] echo $ROS_DISTRO


# Test - talker & listener


> {ros_#1_shell} ros2 run demo_nodes_cpp talker

> [ros_#2_shell] ros2 run demo_nodes_py listener


# Test - turtlesim

> [ros_#1_shell] ros2 run turtlesim turtlesim_node

> [ros_#2_shell] ros2 run turtlesim turtle_teleop_key


