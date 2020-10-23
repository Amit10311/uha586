
Simulation Launch
-----------
# 1. Installation  
Instruction for the installation given in Installation.md file. 

# Aim of  hector-moveit
Hector Quadrotor with MoveIt! Motion Planning Framework.

This project aims a generic application that can autonomously manipulate a quadcopter.

In order to implement Motion Planning primitives, MoveIt! framework is being used in dynamic obstacles environment .


```Shell
sudo apt-get install gazebo9 libgazebo9-dev ros-melodic-gazebo9*
```

```Shell
rosdep install --from-paths src --ignore-src -r -y --rosdistro melodic
```

After that, the repository should be cloned with all its submodules:

```Shell
git clone --recurse-submodules https://github.com/tahsinkose/hector-moveit.git
```

Since, Github does not support partial submoduling yet, the package `hector_gazebo_termal_camera` should be deleted after above command is executed.

In order to build the project execute `catkin build`. Since there are roughly 30 packages, build time may be around 5 minutes.  
To run the project, launch consecutively: 
```Shell
roslaunch hector_moveit_gazebo orchyard_navigation.launch
```

```Shell
roslaunch hector_moveit_exploration explore.launch
```


## What is New?
 Referenced projects and the several others not referenced directly but have similar context use only GUI. As known, despite being a moderately skilled one, MoveIt! GUI is there for just testing purposes. 

## Simulation View
<img src="/images/garden4.jpg" alt="Garden View" width="435" height="435"/><img src="/images/garden5.jpg" alt="Garden View" width="435" height="435"/>
<img src="/images/garden6.jpg" alt="Garden View" width="435" height="435"/><img src="/images/garden7.jpg" alt="Garden View" width="435" height="435"/>
<img src="/images/garden_sky1.jpg" alt="Garden View" width="435" height="435"/><img src="/images/garden_sky2.jpg" alt="Garden View" width="435" height="435"/>
### Exploration v1
[![Orchard Exploration](http://img.youtube.com/vi/ZWn9N9Y_tb8/0.jpg)](https://www.youtube.com/watch?v=ZWn9N9Y_tb8 "Orchard Exploration")

### Exploration v2
Exploration version 2 is explained in further detail in the Development log. In summary, missions that were postponed into this version are implemented except one particular mission. According to the log, orientation fixation and trajectory action is succesfully implemented. Only task delayed to version 3 is the grid approach. Also, a very simple metrics is devised to quantify the success of the stack itself. Initial statistics are outlined in <a href="https://discourse.ros.org/t/precision-agriculture-simulation-with-a-quadcopter-in-gazebo/6025/5?u=tahsin_kose">this comment</a>. They are very important and will provide the basis for enhancements on version 3.



## References
<a href="https://github.com/wilselby/ROS_quadrotor_simulator">ROS Quadrotor Simulator by Wil Selby</a>

<a href="https://github.com/AlessioTonioni/Autonomous-Flight-ROS">Autonomous Flight by Alessio Tonioni</a>

<a href="https://github.com/RiccardoGrin/darknet">Darknet Retraining with Custom Dataset by Riccardo Grin</a>

_**Note**: If you know other similar projects that have the same context with the proposed ability, please inform me so that I can list them as a reference._
