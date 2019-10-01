# paper-plume-positions-data
Input and data files for the manuscript 'Ancient subducted oceans controlling the positioning of deep mantle plumes'. 
These files can be used to reproduce the reults presented in the manuscript, together with the freely available modeling code ASPECT <aspect.geodynamics.org>.

We have used ASPECT version 2.0.0-pre [commit 572f967](https://github.com/geodynamics/aspect/tree/572f9673a183c0975ceac85ea342750e8c2d1930). 

We have used the plate recostruction published in 

> Matthews et al.
> Global plate boundary evolution and kinematics since the late paleozoic.
> *Global  and  Planetary  Change* **146**, 226–250 (2016)

and we provide these files in a format that can be read in by ASPECT in the folder [Matthews_410](./Matthews_410). 

In addition to the plate reconstruction, ASPECT also needs tables that provide all material poperties. 
These tables have been generated using Perple_X as described in the manuscript, and we provide them here
in the folder [look-up_tables](./look-up_tables). 
In order for ASPECT to find them upon the tsart of the model run, they need to be copied into the appropraite 
data repository located in the source directory of an installed version of ASPECT. 


For the [high-resolution model](./input_files/global_convection_3d_stabilization_big.prm), we have used a faster, more recent version of ASPECT (version 2.2.0-pre [commit ec4c65d](https://github.com/jdannberg/aspect/releases/tag/paper-plume-positions-data). 




