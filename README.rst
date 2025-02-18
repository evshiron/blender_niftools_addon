The Blender Niftools Addons enables Blender to import and export NetImmerse files including ``.nif`` and ``.kf``.

Intro
------------

This repo contains fixes to build latest Blender Niftools Addon, which I have spent hours to figure out.

Many thanks to `@Candoran2 <https://github.com/Candoran2>`_, `@TagnumElite <https://github.com/TagnumElite>`_ and Niftools contributors.

.. code-block:: shell

  # with docker and docker-compose installed

  git clone --recursive https://github.com/evshiron/blender_niftools_addon.git
  cd blender_niftools_addon/install

  # makezip.bat wasn't fixed
  bash makezip.sh

  # show built addon zip files
  ls temp/*.zip

Requirements
------------

* `Blender <http://www.blender.org/download/get-blender/>`_

Download
--------

* Release downloadable from `https://github.com/niftools/blender_niftools_addon/releases
  <https://github.com/niftools/blender_niftools_addon/releases>`_ 
  
Currently we are working towards a v1.0.0, so although there is no stable releases of Blender Niftools Addon, each
milestone release will bring more features.

Documentation
-------------

* For full Online documentation, visit `https://blender-niftools-addon.readthedocs.io 
  <https://blender-niftools-addon.readthedocs.io>`_
* For a list of changes between versions, see `Changelog <CHANGELOG.rst>`_
* See `How to Contribute <CONTRIBUTING.rst>`_ for a list of contribution rules.

Support
-------

`Changelog <CHANGELOG.rst>`_

Issues
------

* Check the Blender Niftools Addon repository's for existing issue `Issue tracker 
  <http://github.com/niftools/blender_niftools_addon/issues>`_
* If the issue has not been reported please create a new report, filling in the template **completely**.

Fork
----

.. code-block:: shell
  
  git clone --recursive git://github.com/niftools/blender_niftools_addon.git
