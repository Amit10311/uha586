# 1. Aim
Provinding the obj file to the drone having the Real world Environment.
* Input: .gml file
* Results: .obj file


## 1. Sketchup
* Step1: Run the sketchup 

* Step2: Select Template
```
The urban planning -Meters 
```

* Step3: Import gml file 
```
File > Import > Input_file_gmlfiles/38**_581*/38*0_581*.gml
```
12 Input files  with .gml extension 
```
$ cd ~/Maps/Input_file_gmlfiles/38*0_581*/38**_58**.gml
```

* Step4: Export 3D Model 
```
File > Export > 3D Model >   Maps/Output_files/38**_city/38*0_581*/38*0_581.skp
```

* Step5: Import  Model 
```
File > Import > 3D Model >   Maps/Output_files/38**_city/38*0_581*/38*0_581.skp
```

* Step 6: rendering   Model 

 Insert color or image 

> * the Getting Started toolbar, click the Paint Bucket tool ().
* In the Materials panel that appears, select Colors from the drop-down menu, as shown here. Then select a color from the options that appear on the Select tab.

```
Materilas > Select > Image 
```

* Step7: Export 3D Model to obj
```
File > Export > 3D Model > Maps/Output_files/38**_city/38*0_581*/*0_1*.obj
```

``` Output files 
Output_files/38*0_city/38*0_581*/*0_1*.obj
Output_files/38*0_city/38*0_581*/*0_1*.mtl
```
``` example files 
Output_files/3850_city/3850_5816/50_16.obj
Output_files/3850_city/3850_5816/50_16.mtl
```
## 2. Meshlab

You can open the files in Meshlab and see the structure 
``` Output files 
Output_files/38*0_city/38*0_581*/*0_1*.obj
```

## 3. Structure info 
``` Info  files 
Output_files/38*0_city/info.txt
```
``` Example 
3850_5817.obj
object count 326
width 507.73 height 1038.08
```
