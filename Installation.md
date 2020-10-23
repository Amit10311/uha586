Installation
===============

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

2. Remove Gazebo 7 and all related packages, and then install Gazebo 9:


```console
$ sudo apt-get remove ros-kinetic-gazebo* gazebo* libgazebo*
$ sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable `lsb_release -cs` main" > /etc/apt/sources.list.d/gazebo-stable.list'
$ wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -
$ sudo apt-get update
$ sudo apt-get install gazebo9 gazebo9-* ros-kinetic-gazebo9-*
$ sudo apt upgrade
$ gazebo
```

> **Note** Remove library files of gazebo old version`libgazebo*`will give you problem while running gazebo.

 3. Additional packages are required to build the package.

```console
$ sudo apt-get install libeigen3-dev ros-kinetic-image-view libprotobuf-dev libprotoc-dev ros-kinetic-nav-msgs ros-kinetic-mav-msgs libyaml-cpp-dev ros-kinetic-nodelet ros-kinetic-mav-planning-msgs ros-kinetic-urdf ros-kinetic-image-transport ros-kinetic-roslint ros-kinetic-angles ros-kinetic-tf2-geometry-msgs ros-kinetic-xacro ffmpeg libavcodec-dev libavformat-dev libavutil-dev libswscale-dev ros-kinetic-camera-info-manager ros-kinetic-cmake-modules ros-kinetic-gazebo-msgs ros-kinetic-mavros-msgs ros-kinetic-control-toolbox ros-kinetic-mav-msgs ros-kinetic-libmavconn ros-kinetic-mavros ros-kinetic-octomap-msgs ros-kinetic-geographic-msgs ros-kinetic-mavlink ros-kinetic-mavros-extras ros-kinetic-mav-planning-msgs ros-kinetic-jsk-visualization
```

4. If you don't have ROS workspace yet you can do so by

```console

$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/src
$ catkin_init_workspace  # initialize your catkin workspace
$ cd ~/catkin_ws/
$ catkin init
$ cd ~/catkin_ws/src
```
5. Copy packages from **crazy_uav** folder 
```
cp -R ~/crazy_uav/src/load_octomap/ ~/catkin_ws/src
cp -R ~/crazy_uav/src/CrazyS/ ~/catkin_ws/src
```

```
$ cd ~/catkin_ws/src
$ git clone  https://github.com/OctoMap/octomap_mapping.git
$ git clone -b crazys https://github.com/gsilano/mav_comm.git
$ cd ~/catkin_ws/src/mav_comm
$ git checkout med18_gazebo9
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
```
Note In case the ERROR[rotors_gazebo_plugins] error is displayed, run the following commands

```
$ sudo apt-get install ros-kinetic-gazebo9-plugins
$ sudo apt-get install apt ros-kinetic-gazebo9-ros
$ sudo apt-get install apt ros-kinetic-gazebo9-dev
```
