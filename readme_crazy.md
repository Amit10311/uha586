
Simulation Launch
-----------
There are two simulation files with a visual-inertial sensor and without it. The following are commands to run the simulations. 

```console 1
$ cd ~/crazy_uav/src
$ catkin_make
$ source devel/setup.bash
```

```console 1
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ rotors_gazebo mav_with_berlin_waypoint_with_vi_sensor.launch
```

```console 2
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ roslaunch rotors_gazebo mav_with_berlin_waypoint_publisher.launch
```
