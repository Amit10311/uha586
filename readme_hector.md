
Simulation Launch
-----------
# 1. Installation  
Instruction for the installation given in Installation.md file. 

# Aim of  hector-moveit
Hector Quadrotor with MoveIt! Motion Planning Framework.

This project aims a generic application that can autonomously manipulate a quadcopter.

In order to implement Motion Planning primitives, MoveIt! framework is being used in dynamic obstacles environment .

* The package `hector_gazebo_termal_camera` should be deleted after above command is executed.

 Since there are roughly 30 packages, build time may be around 5 minutes.  
To run the project, launch consecutively: 
Shell 1
```Shell
roslaunch hector_moveit_gazebo orchyard_navigation.launch
```
Shell 2
```Shell
roslaunch hector_moveit_exploration explore.launch
```

Shell 1
```Shell 3 
roslaunch hector_moveit_gazebo world_test.launch
```





## References
<a href="https://github.com/wilselby/ROS_quadrotor_simulator">ROS Quadrotor Simulator by Wil Selby</a>

<a href="https://github.com/AlessioTonioni/Autonomous-Flight-ROS">Autonomous Flight by Alessio Tonioni</a>

<a href="https://github.com/RiccardoGrin/darknet">Darknet Retraining with Custom Dataset by Riccardo Grin</a>

_**Note**: If you know other similar projects that have the same context with the proposed ability, please inform me so that I can list them as a reference._
