Simulation Launch
-----------
# 1. Insatllation  
Instruction for the installation given in Installation.md file. 


# 2. Run the Simulation 
There are two simulation files with a visual-inertial sensor and without it. The following are commands to run the simulations. 

```console 1
$ cd ~/crazy_uav/src
$ catkin_make
$ source devel/setup.bash
```
## 2.1 Run the Way-point  Simulation 
```console 1
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ roslaunch rotors_gazebo mav_with_berlin_waypoint_publisher.launch
```
To know the structure of simulation  
```console 2
$ rosrun rqt_graph rqt_graph 
```

## 2.2 Simulation with  Way-point  Simulation  vi Sensor for Mapping

```console 1
$ cd ~/crazy_uav/src
$ source devel/setup.bash
$ rotors_gazebo mav_with_berlin_waypoint_with_vi_sensor.launch
```
To know the structure of simulation  
```console 2
$ rosrun rqt_graph rqt_graph 
```


