.. note::
   This manual is still under development and there could be some incomplete parts, marked as 'Work in progress'.

========================
SimVisSuite Introduction
========================

**SimVisSuite** is an integrative visualization framework developed for the HBP providing a set of strategies for generating images that facilitate the exploration of neuronal datasets at different spatio-temporal scales and from different perspectives (structural, functional, and connectivity). It also provides specific solutions for combining the generated images, corresponding to data at different scales and perspectives, presenting them in a combined way through a multiple coordinated views mechanism. 

This approach gives a powerful interactive visualization environment, very helpful for the analysis of complex datasets. More specifically, the framework provides different views allowing the exploration of neuronal morphology, neuronal activity, and neuronal connectivity at the same time with the same dataset. Since the brain is inherently a multiscale system, it provides interactive visualizations at different levels of abstraction. This multilevel approach helps managing complexity and linking phenomena taking place at different organizational levels.

This framework, called SimVisSuite, is composed of three modules: ViSimpl, NeuroTessMesh and NeuroScheme (ConGen).

In this documentation we'll give details about its dependencias and explain how to compile and develop for SimVisSuite.

---------------------
Hardware requirements
---------------------

SimVisSuite requires a graphic card that supports OpenGL 3.3 at least. It is also recommended (depending on dataset size) to use a multi-core CPU for parallel processing deployment. The size of the datasets that the applications of SimVisSuite is able to load depends on the available memory on the machine.

--------------
External Links
--------------

In `Ebrains website`_ :

* `NeuroScheme Ebrains page`_.
* `NeuroTessMesh Ebrains page`_.
* `ViSimpl Ebrains page`_.

In `Visualization and Graphics Lab website`_ :

* `NeuroScheme VG-Lab homepage`_.
* `NeuroTessMesh VG-Lab homepage`_.
* `ViSimpl VG-Lab homepage`_.

The source code for the lastest release are available in the Github pages. For reporting bugs please use the Issues page from the application repository page.

* `NeuroScheme Github repository`_.
* `NeuroTessMesh Github repository`_.
* `ViSimpl Github repository`_.

If you have any questions or suggestions about SimVisSuite and its applications development email to dev@vg-lab.es.

.. _Ebrains website: https://www.ebrains.eu/
.. _NeuroScheme Ebrains page: https://www.ebrains.eu/tools/neuroscheme
.. _NeuroTessMesh Ebrains page: https://www.ebrains.eu/tools/neurotessmesh
.. _ViSimpl Ebrains page: https://www.ebrains.eu/tools/visimpl
.. _Visualization and Graphics Lab website: https://vg-lab.es
.. _NeuroScheme VG-Lab homepage: https://vg-lab.es/neuroscheme/index.html
.. _NeuroTessMesh VG-Lab homepage: https://vg-lab.es/neurolots/
.. _ViSimpl VG-Lab homepage: https://vg-lab.es/visimpl/
.. _NeuroScheme Github repository: https://github.com/vg-lab/NeuroScheme
.. _NeuroTessMesh Github repository: https://github.com/vg-lab/NeuroTessMesh
.. _ViSimpl Github repository: https://github.com/vg-lab/visimpl

----------------------------------------
SimVisSuite applications synchronization
----------------------------------------

For SimVisSuite applications to synchronize events and views a discovery provider service must be installed in the machine(s) running the applications. This synchronization method allows the applications to _discover_ each other without the need of any configuration from the user. 
This discovery method is based on ZeroConf protocol and is provided by Avahi service on Linux and dnssd on Mac and Windows machines (like `Bonjour <https://developer.apple.com/bonjour/>`_).

If that service is not present the applications will still be usable but won't be able to synchronize and communicate.

------------------------
Installation and running
------------------------

Please refer to the homepage of the applications for instructions on how to install and run, either as a native executable or as the provided docker images. 

^^^^^^^^^^^^^^^^^
Docker containers
^^^^^^^^^^^^^^^^^

The docker containers for **SimVisSuite** aplications can be found on `Docker Hub`_. It's recommended to use the highest tag number (latest official release) or the **git master** (represents the latest commit to master branch, and usually are the same as the highest tag number).

.. _Docker Hub: https://hub.docker.com/u/vglab

