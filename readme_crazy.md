Simulation Launch
-----------
# 1. Installation  
Instruction for the installation given in Installation.md file. 

# 2. Aim
## 2.1 Follow the waypoint 
Provinding the Waypoint to the drone with the Real world Environment Simulation.

Results: Follow the waypoint 

# 3. Run the Simulation 
There are two simulation files with a visual-inertial sensor and without it. The following are commands to run the simulations. 

```console 1
$ cd ~/crazy_uav/
$ catkin_make
$ source devel/setup.bash
```

## 3.1 Run the Way-point  Simulation 
* Start waypoints: x=1 y=171 z=6
* End waypoints: x=241 y=81 z=34
```console 1
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ roslaunch rotors_gazebo mav_with_berlin_waypoint_publisher.launch
```
To know the structure of simulation  
```console 2
$ rosrun rqt_graph rqt_graph 
```

To know the information about Nodes,  the currently running Nodes. 
```console 3
$ rosnode list
```
```Output
/gazebo
/gazebo_gui
/pelican/Goal
/pelican/initial_marker
/pelican/joint_state_publisher
/pelican/lee_position_controller_node
/pelican/pictogram_demo
/pelican/robot_state_publisher
/pelican/rviz
/rosout
```

Inpput files of simulation  
```console 4
$ cd ~/crazy_uav/src
$ cd CrazyS/rotors_gazebo/resource/
$ cat berlin_path_way.txt
```
```
$ cd ~/crazy_uav/src
$ cd CrazyS/rotors_gazebo/worlds/
$ cat berlin.world
```

Launch file to provide inputs
```
$ cd ~/crazy_uav/src
$ cd CrazyS/rotors_gazebo/worlds/
$ cat mav_with_berlin_waypoint_publisher.launch.world
```


## 3.2 Simulation with  Way-point  Simulation  vi Sensor for Mapping ( Starting waypoints: x=1 y=171 z=6)


```console 1
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ rotors_gazebo mav_with_berlin_waypoint_with_vi_sensor.launch
```
To know the structure of simulation  
```console 2
$ rosrun rqt_graph rqt_graph 
```
## 3.3 Simulation with  Way-point  Simulation  in long world ( Starting waypoints: x=1 y=1031 z=6)
* Start waypoints: x=1 y=1031 z=6.7
* End waypoints: x=851 y=221 z=81.85
 
```console 1
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ roslaunch rotors_gazebo mav_with_long_world.launch 
```
To know the structure of simulation  
```console 2
$ rosrun rqt_graph rqt_graph 
```

Input files of simulation  
```console 3
$ cd ~/crazy_uav/src
$ cd CrazyS/rotors_gazebo/resource/
$ cat berlin_long_path.txt
```
```console 3
$ cd ~/crazy_uav/src
$ cd CrazyS/rotors_gazebo/launch/
$ cat mav_with_long_world.txt
```

Launch file to provide inputs
```
$ cd ~/crazy_uav/src
$ cd CrazyS/rotors_gazebo/worlds/
$ cat mav_with_long_world.launch.world
```



