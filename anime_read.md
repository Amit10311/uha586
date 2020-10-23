# 1. Aim
Package to add motion to dae files to hector simulation 

Results: Objects in motion

# 2. Setup


```console 1
cd ~/gazebo_animatedbox_tutorial
mkdir build
cd build
cmake ../
make
```
# 3. Make sure Gazebo can load the plugins later
```console 1
export GAZEBO_PLUGIN_PATH=`pwd`:$GAZEBO_PLUGIN_PATH
```
# 4. Simulate with gazebo
Run using gazebo itself with:
```console 1
cd ~/gazebo_animatedbox_tutorial
gazebo animated_box.world
```
In another terminal, use "gz topic" user interface to view the pose:
```console 2
gz topic -v /gazebo/animated_box_world/pose/info
```


