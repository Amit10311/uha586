
Simulation Launch
-----------
# 1. Installation  
Instruction for the installation given in Installation.md file. 

# Aim of  hector-moveit 
Hector Quadrotor with MoveIt! Motion Planning Framework.
1. Explore planning in static environment 

2. Explore planning in dynamic environment 

Output : Too slow for motion planning 


This project aims a generic application that can autonomously manipulate a quadcopter.

In order to implement Motion Planning primitives, MoveIt! framework is being used in dynamic obstacles environment .

* The package `hector_gazebo_termal_camera` should be deleted after above command is executed.

 Since there are roughly 30 packages, build time may be around 5 minutes.  
 
# 2. Static Environment 
To run the project, launch consecutively: 
Shell 1
```Shell
cd ~/hector/
catkin_make
source devel/seteup.bash
roslaunch hector_moveit_gazebo berlin_navigation.launch
```
Shell 2
```Shell
cd ~/hector/
catkin_make
source devel/seteup.bash
roslaunch hector_moveit_exploration explore.launch
```


# 3. Dynamic Environment 

Shell 1
```Shell 1 
cd ~/hector/
catkin_make
source devel/seteup.bash
roslaunch hector_moveit_gazebo world_test.launch
```

Shell 1
```Shell 1 
cd ~/hector/
catkin_make
source devel/seteup.bash
roslaunch hector_moveit_gazebo Motion_Environment.launch
```

Shell 2
```Shell 2
cd ~/hector/
catkin_make
source devel/seteup.bash
roslaunch hector_moveit_exploration explore.launch
```



## References
<a href="https://github.com/wilselby/ROS_quadrotor_simulator">ROS Quadrotor Simulator by Wil Selby</a>

<a href="https://github.com/AlessioTonioni/Autonomous-Flight-ROS">Autonomous Flight by Alessio Tonioni</a>

<a href="https://github.com/RiccardoGrin/darknet">Darknet Retraining with Custom Dataset by Riccardo Grin</a>

