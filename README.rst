
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
  
**To use MATLAB mex interface:**

.. code-block:: matlab
  
	  bet2_mex(input)
where input is a 3D single real array. 
  
**To use in Python:**

.. code-block:: python

      import ctypes
      handle = ctypes.CDLL(os.path.join(dir_path, "lib", "libbet2.so"))
      handle.runBET.argtypes = [np.ctypeslib.ndpointer(np.float32, ndim=self.img_mag.ndim, flags='F'),
                      np.ctypeslib.ndpointer(np.float32, ndim=len(mask_size), flags='F'),
                      ctypes.c_int, ctypes.c_int, ctypes.c_int]
      mask_size = mag.shape
      mag = self.img_mag.copy(order='F')
      mask = np.zeros(mask_size, dtype=mag.dtype, order='F')
      handle.runBET(mag, mask, *mask_size)

where input is a 3D float32 real numpy array. 		

 

Precompiled mex files for Windows and Linux can be downloaded in the repository releases.
