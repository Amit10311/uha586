# publish_pointcloud
this code can be used for transfom the pointcloud into octomap

## Build the ROS workspace   
```
cd cloud_pkg/src
catkin_make
``` 
# Dependencies
```
git clone https://github.com/OctoMap/octomap_mapping.git
``` 

Place the test.pcd file from the folder data in the catkin_ws directory, and modify the launch file to specify the directory where test.pcd is located.

## Start the transformation node
    roslaunch publish_pointcloud demo.launch  
