===================
bet2
===================
standalone Brain Extraction Tool (bet2) with python wrapper, released by http://fsl.fmrib.ox.ac.uk/

The following features are added:

 * The program is reconfigured using CMake
 * CMake configures MATLAB mex target as well.
 * Building static and dynamic library (dll or so) of BET
 * Support Windows and Linux

To build:

.. code-block:: bash

  git clone https://github.com/aghaeifar/bet2.git
  mkdir build
  cd build
  cmake ..
  make -j4
  
To use:

.. code-block:: matlab
  
  bet2_mex(input)
  
  
where input is a **3D single real** array.  

Precompiled mex files for Windows and Linux can be downloaded in the repository releases.
