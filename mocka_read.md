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
```
!-- map size unit meter-->
  <param name="x_length" type="int" value="300"/>
  <param name="y_length" type="int" value="300"/>
  <param name="z_length" type="int" value="30"/>
  
```

Reading about pacakge: https://arxiv.org/pdf/1906.09785.pdf
