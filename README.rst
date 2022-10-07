
# bet2
standalone Brain Extraction Tool (bet2) with MATLAB mex wrapper, released by http://fsl.fmrib.ox.ac.uk/

The following features are added:

 * the program is reconfigured using CMake
 * CMake configures MATLAB mex target as well.
 * Support Windows and Linux

to compile source code:

     mkdir build
     cd build
     cmake ..
     make

 
 to use:
 

    bet2_mex(input)
input should be a **3D single real** array.
Precompiled mex files for Windows and Linux can be downloaded in the repository releases.
