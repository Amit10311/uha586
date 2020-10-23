Simulation Launch
-----------
# 1. Installation  
Instruction for the installation given in Installation.md file. 

# 2. Aim
## 2.1 Provide the octmap for moveit planner in hector  
Provinding the Waypoint to the drone with the Real world Environment Simulation.
* Input:  Octomap
* Results: Provide the octomap info simulation 

# 3.1 Run the Simulation 1

```console 1   Build the package 
$ cd ~/octo_world
$ catkin_make
$ source devel/setup.bash
$ roslaunch load_octomap load_octomap.launch 
```
Output 

```console 2 Output  
$ rosrun rviz rviz 
```


Input files of simulation  

Octomap=> 3880_5818.bt
```console 3
$ cd ~/octo_world/src/larics_gazebo_worlds/models/berlin/
$ cat 3880_5818.bt
```


Launch file to provide inputs
```
$ cd ~/octo_world/src
$ cd load_octomap/launch/
$ cat load_octomap.launch
```
Source Code to publish octomap to moveit 
```
$ cd ~/octo_world/src/
$ cat octoload.py
```


# 3.2 Run the Simulation 2
```console 1   Build the package 
$ cd ~/octo_world
$ source devel/setup.bash
$ roslaunch load_octomap load_octomap_long.launch 
```
Output 

```console 2 Output  
$ rosrun rviz rviz 
```

Input files of simulation  

Octomap=> 3860_5817.bt
```console 3
$ cd ~/octo_world/src/larics_gazebo_worlds/models/berlin_60_17"/>
$ cat 3860_5817.bt
```
