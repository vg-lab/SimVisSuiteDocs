=======================
SimVisSuite Development
=======================

---------------------
Software requirements
---------------------

**SimVisSuite** applications are developed in the C++ using the C++11 standard. The basic requirements to compile the applications are:

* C++11 compiler: `gcc on Linux`_ or `Mingw64 on Windows`_ machines.
* `CMake`_ build tool: at least version 3.0.0
* `Git`_ distributed version control tool.

.. _gcc on Linux: https://gcc.gnu.org/
.. _Mingw64 on windows: https://www.mingw-w64.org/
.. _CMake: https://cmake.org/
.. _Git: https://git-scm.com/

The C++ standard is set by default by the ``CMake/Common`` package included in all applications and some dependencies. If modifications to the source code requires a C++ standard higher than C++11 that can be applied by overriding the CMake variable ``CMAKE_CPP_FLAGS`` after the ``common_find_package_post()`` command in the ``CMakeLists.txt`` build script.

------------
Dependencies
------------

In overview, the SimVisSuite applications depend on the following external libraries to provide some of its functionalities:

* UI, 3D visualization and general purpose:

  * `Qt`_: Cross-platform graphical library and tools.
  * `Boost`_: general purpose C++ libraries.
  * `scoop`_: library to implement and manage color palettes and value-mappers.
  * `AcuteRecorder`_: library that implements a video/screenshot recorder to capture the contents of a Qt Widget.
  * `ReTo`_: library that implements auxiliary tools for 3D rendering.  
  * `plab`_: library that implements a fast particle rendering engine.
  * `GLM`_: OpenGL Mathematics library.
  * `GLEW`_: OpenGL Extension Wrangler Library. 
  * `GLUT`_: OpenGL utility toolkit library.
  * `ShiFT`_: library based on `FiReS`_ to implement properties and data structures to define relationships between entities.
  * `Eigen3`_: template library for linear algebra operations.

* NeuroScience related:

  * `Brion`_: library to read and write access to Blue Brain data structures.
  * `nsol`_: library that provides data structures to handle basic neuroscientific data, mainly cortex morphologies and its structures.
  * `SimIL`_: library to read brain simulation datasets in BlueConfig, HDF5 and CSV formats.
  * `HDF5`_: library that implement the HDF5 data model read and write operations.
  * `NeuroLOTs`_: set of libraries and tools for generating neuronal meshes and for visualizing them at different levels of detail using GPU-based tessellation.
    
* Connectivity and Network:

  * `ZeroEQ`_: library for modern messaging using ZeroMQ that also integrates REST APIs with JSON payload.
  * `Lexis`_: library to implement a vocabulary used for event-driven communication in and between visualization software.
  * `gmrvLex`_: library that implements the vocabulary for event-driven communication between SimVisSuite applications using Lexis.

.. _Brion: https://github.com/BlueBrain/Brion  
.. _ZeroEQ: ttps://github.com/HBPVis/ZeroEQ
.. _Lexis: https://github.com/HBPVis/Lexis
.. _gmrvLex: https://github.com/vg-lab/gmrvlex
.. _ShiFT: https://github.com/vg-lab/shift
.. _FiReS: https://github.com/vg-lab/FiReS
.. _scoop: https://github.com/vg-lab/scoop
.. _Eigen3: https://eigen.tuxfamily.org/
.. _ReTo: https://github.com/vg-lab/ReTo
.. _SimIL: https://github.com/vg-lab/SimIL
.. _plab: https://github.com/vg-lab/particlelab
.. _GLM: https://github.com/g-truc/glm
.. _GLEW: https://glew.sourceforge.net/
.. _HDF5: https://github.com/HDFGroup/hdf5
.. _NeuroLOTs: https://github.com/gmrvvis/neurolots
.. _GLUT: https://www.opengl.org/resources/libraries/glut/glut_downloads.php
.. _Boost: https://www.boost.org/
.. _Qt: https://www.qt.io/
.. _nsol: https://github.com/vg-lab/nsol
.. _AcuteRecorder: https://github.com/vg-lab/AcuteRecorder


Some of those libraries have already other dependencies that must be fulfilled to compile a feature complete SimVisSuite in the selected platform.

Not all libraries are strictly needed, some implement optional funcionalities that can be disabled when compiling a SimVisSuite application depending on the needs. In the following chapters of this documentation the possible compilation options and the libraries required for them are described in detail in the compilation part of each application.

-----------
Compilation
-----------

The compilation requeriments, procedure and possible CMAKE flags is detailed in the next chapters of this documentation for each of the applications that comprise SimVisSuite.

--------------------
Compilation problems
--------------------

While SimVisSuite applications code compile without modifications some of its dependencies can report problems compiling in newer versions of the compilers. The possible solutions are:
* Override warnings either modifying the compiler flags or adding ``#pragma`` preprocessor directives in the offending source code files.
* Manually fix the problems updating the code to the new standard requirements. 

The latter option is recommended as most of the problems (like deprecated methods or ``CASE`` without ``break;`` warnings) are very easy to fix that way.

