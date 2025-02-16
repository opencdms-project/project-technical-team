Master data
===========

The master data schema contains both metadata and the observational data, with the metadata based on the WIGOS metadata
standard and the WMO Core Metadata Profile. The figure below shows an overview of the relationships between the
observations and metadata tables, including the relationship with the WIGOS Metadata Standard and the WMO Core Metadata Profile.

.. plantuml:: ./master_data.puml

Each of the components shown in the figure above link to one or more additional tables.
These are described further in the sections below.

Host
----

The *host* and associated tables provide information on the observing facility or station associated with an observation.
This includes information such as: the geospatial location of the host and changes in time; the environment where the
host is located; which observing programs the host may be associated with; a log of events at the observing facility;
any associated media such as reports or images; and a list of known aliases for the host.
The figure below shows the primary links for the associated host tables.

.. plantuml:: ./host.puml

The pages linked below define each of the associated tables, including the *host* table.

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: Associated tables:

   master_data/host*
   master_data/reference_station


Equipment
---------

The *equipment* and associated tables provide information on equipment registered in the climate data management system
and that may be associated with one or more hosts. The equipment may be a sensor used to make observations or another
piece of equipment such as a Stevenson screen used to house wet and dry bulb thermometers. As with the *host*, each item
of *equipment* can have an associated log providing a record of events associated with the equipment, for example
a sensor may have been sent for calibration.

.. plantuml:: ./equipment.puml

The pages linked below define each of the associated tables, including the *equipment* table.

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: Associated tables:

   master_data/equipment*
   master_data/sensor_characteristics

Deployment
----------

The *deployment* table provides information on the installation of a piece of equipment as a given host or
observing facility. This includes: the deployment location; installation height and configuration; expected quality
information; maintenance schedule; etc. The associated tables provide information on the operating status
of the deployed equipment, which application area is the primary purpose of the observations, a log of events
associated with the deployment and any associated media (e.g. photographs of the deployed equipment *in situ*).


.. plantuml:: ./deployment.puml

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: Associated tables:

   master_data/deployment*
   master_data/operating_status

Observation
-----------

The *observation* table contains the observations stored within the database and has been developed based on the
Open Geospatial Consortium (OGC) *Observations, Measurements and Samples* standard (OGC-OMS). Each record contains
information on a single discrete observation, including: what is being observed, the result of the observation and its units;
the spatial and temporal bounds associated an observation; quality flags; instance level metadata;
which sensor (equipment) and / or host is associated with the observation etc. The full definition of the
table can be found via the link below.

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: Observation table definition:

   master_data/observation


Feature
-------

In addition to being associated with a host or sensor, each observation can be associated with a feature of interest.
The *Feature* table contains all the features of interest defined and registered within the CDMS. The definition of
the table can be found via the link below.

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: Feature table definition:

   master_data/feature

Source
------

The source table is used to record where the observations have come from, for example a source data file,
an external service etc.

The definition of
the table can be found via the link below.

.. toctree::
   :maxdepth: 1
   :glob:
   :caption: Source table definition:

   master_data/source
