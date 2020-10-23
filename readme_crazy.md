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
$ cd ~/crazy_uav/src
$ catkin_make
$ source devel/setup.bash
```
## 3.1 Run the Way-point  Simulation ( Starting waypoints: x=1 y=171 z=6)

```console 1
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ roslaunch rotors_gazebo mav_with_berlin_waypoint_publisher.launch
```
To know the structure of simulation  
```console 2
$ rosrun rqt_graph rqt_graph 
```
Inpput files of simulation  
```console 3
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

```console 1
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ roslaunch rotors_gazebo mav_with_long_world.launch 
```
To know the structure of simulation  
```console 2
$ rosrun rqt_graph rqt_graph 
```

Inpput files of simulation  
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



