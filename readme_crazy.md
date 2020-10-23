
Simulation Launch
-----------

```console
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
There are two simulation files with a visual-inertial sensor and without it. The following are commands to run the simulations. 
```

```console
$ roslaunch rotors_gazebo mav_with_berlin_waypoint_with_vi_sensor.launch
```

```console
$ roslaunch rotors_gazebo mav_with_berlin_waypoint_publisher.launch
```
