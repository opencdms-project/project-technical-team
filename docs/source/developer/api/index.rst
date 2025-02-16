OpenCDMS API
============

The API within OpenCDMS is built using `pygeoapi <https://docs.pygeoapi.io/en/stable/>`_ and exposes the following APIs.

- `OGC API - Features <https://ogcapi.ogc.org/features/>`_
- `OGC API - Records <https://ogcapi.ogc.org/records/>`_
- `OGC API - Processes <https://ogcapi.ogc.org/processes/>`_

This section describes the OGC-API processes that have been developed and implemented as part of OpenCDMS. The
Features and Records are defined under the database section.


OGC API - Processes
-------------------
.. toctree::
   :maxdepth: 1
   :caption: Contents:

   automated_quality_control/index
   encode_daycli/index

Cookie cutter
-------------

To help generate new OGC-API Process plugins a Python package template has been created for use with the Python
`cookiecutter <https://cookiecutter.readthedocs.io/en/stable/>`_ module. The module can be installed using the command:

.. code::

    `pip3 install cookiecutter`.

Once installed the cookiecutter can be used with:

.. code::

   cookiecutter gh:opencdms/pygeoapi-process-cookiecutter

The following prompt will be displayed:

.. code::

   author [Name of author]:
   email [Author email address]:
   maintainer [Name of maintainer]:
   maintainer_email [Maintainer email address]:
   package_url [Package homepage]:
   package_name [Name of python package to create, e.g. import {package_name}]:
   process_id [ID for process, e.g. /processes/{process_id}]:
   process_class_name [Name of process class, {package_name}.{process_name}]:
   process_description [Short description of process]:
   keywords []:
   license [APL2]:

Following entry of the requested information this will create a python package for an empty pygeoapi process plugin.
The plugin can be installed via the normal route for a Python package, e.g. using `pip3 install <package_name>` for
packages published via PyPI or `python3 setup.py install`.
