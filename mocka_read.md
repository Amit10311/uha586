# mockamap
* Aim: A simple big map generator based on ROS
Results: Map generator


# 1 Installation 
```console 1
$ cd ~/mockamap/build
$ cmake.. 
$ make 
$ source devel/setup.bash 
```


# 3. Run the Simulation 

```console 1  post2d map
$ cd ~/mockamap/build
$ source devel/setup.bash$
$ cd ..
$ roslaunch mockamap post2d.launch 
```

Inpput files of simulation  
```console 2
$ cd ~/crazy_uav/src
$ cd /home/amit/mockamap/launch/post2d.launch 
```
Changes can be made as  required in post2d.launch 
```
!--Change the  number of obsactles  value=" *** " ->
 <node pkg="mockamap" type="mockamap_node" name="mockamap_node" output="screen">
  <param name="seed" type="int" value="511"/>
  
  
!--Change the  map size (unit meter)-->
  <param name="x_length" type="int" value="300"/>
  <param name="y_length" type="int" value="300"/>
  <param name="z_length" type="int" value="30"/>
```

Reading about pacakge: https://arxiv.org/pdf/1906.09785.pdf

# 4 Dependencies of Packages 
1. Point_cloud
2. PointCloud2
3. pcl_conversions
