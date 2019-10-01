# paper-plume-positions-data
Input and data files for the manuscript 'Ancient subducted oceans controlling the positioning of deep mantle plumes'. 
These files can be used to reproduce the reults presented in the manuscript, together with the freely available modeling code ASPECT ([aspect.geodynamics.org](aspect.geodynamics.org)).

The input files are located in the folder [input_files](./input_files), and can be run together with an 
installed version of ASPECT by navigating to the input_files folder in the terminal and typing 
```./aspect input_file.prm```
where `./aspect` is a link to the executable of an installed version of ASPECT, and `input_file.prm` 
is the name of any of the files located in the [input_files](./input_files) folder. 
We have used ASPECT version 2.0.0-pre ([commit 572f967](https://github.com/geodynamics/aspect/tree/572f9673a183c0975ceac85ea342750e8c2d1930)). 

We have used the plate recostruction published in 

> Matthews et al.
> Global plate boundary evolution and kinematics since the late paleozoic.
> *Global  and  Planetary  Change* **146**, 226–250 (2016)

and we provide the plate reconstruction files in a format that can be read in by ASPECT in the folder [Matthews_410](./Matthews_410). ASPECT should automatically find these files using the path provided in the input file. 

In addition to the plate reconstruction, ASPECT also needs tables that provide all material poperties. 
These tables have been generated using Perple_X as described in the manuscript, and we provide them here
in the folder [look-up_tables](./look-up_tables). 
In order for ASPECT to find them upon the start of the model run, they need to be copied into the appropriate 
data repository located in the source directory of an installed version of ASPECT (`$ASPECT_SOURCE_DIR/data/material-model/steinberger/`). 

Finally, the model in the manuscript also needs some additional code that is not in the main version of ASPECT. 
We povide this code here in the form of shared libraries in the folder [shared_libs](./shared_libs). 
These files still need to be compiled after ASPECT is installed, as described in the ASPECT manual under
[6.2 How to write a plugin](http://www.math.clemson.edu/~heister/manual.pdf#sec%3Awrite-plugin), using the option 'Put the `my_plugin.cc` file into a directory of your choice and compile it into a shared library [...]'. 

For the [high-resolution model](./input_files/global_convection_3d_stabilization_big.prm), we have used a faster, more recent version of ASPECT (version 2.2.0-pre [commit ec4c65d](https://github.com/jdannberg/aspect/releases/tag/paper-plume-positions-data)). This also requires an updated version of the shared libraries, located in [shared_libs_2](./shared_libs_2). They need to be compiled in the same way as described above. 




