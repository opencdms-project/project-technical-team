.. _auto_qc:

Automated quality control
=========================
Tests based on the WMO "Guidelines on Surface Station Data Quality Control and Quality Assurance for Climate Applications", WMO-No. 1269.

Overview
--------
The tests listed below are intended to be run automatically on individual observations on initial ingest and will be called
from another process.

Tests
-----

- **Sensor based range check** (detects observations that are outside the specified sensor limits), requires observer and result.
- **Domain test** (determines whether the observed value is outside the realm of scientific possibility, e.g. air temperature > 70 Celsius), requires observed_property and result.
- **Climate based range test** (compares the observed value with the climatological upper and lower extreme values), requires location, elevation, date, time observed_property and result. Sensor characteristics can be taken into account if available.

API definition
--------------

.. openapi:: ./api.yml


Activity diagram
----------------
.. plantuml:: ./activity.puml

Implementation status
---------------------

In development
