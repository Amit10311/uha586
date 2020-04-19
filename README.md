Simulation
===============

We have used ROS package [CrazyS](https://github.com/gsilano/CrazyS), aimed to modeling, developing and integrating the [Pelican](https://robots.ros.org/astec-pelican-and-hummingbird/) quadcopter in the physics based simulation environment Gazebo. 


The platform was developed using Ubuntu 16.04 and the Kinetic Kame version of ROS.

Installation Instructions - Ubuntu 16.04 with ROS Kinetic and Gazebo 9
---------------------------------------------------------
1. Install and initialize ROS kinetic desktop full, 

 ```console
$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
$ sudo apt-get update
$ sudo apt-get install ros-kinetic-desktop-full
$ sudo rosdep init
$ rosdep update
$ echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
$ source ~/.bashrc
$ sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential
 ```
