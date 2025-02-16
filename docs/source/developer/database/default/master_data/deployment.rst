:html_theme.sidebar_secondary.remove:

deployment
====

Download the definition as a CSV file: :download:`csv <deployment.csv>`.

.. csv-table:: Definition of the *deployment* table.
   :header: "Property","Kind","References","Requirement","Description"

   ".. _id:

   id","str",,"Required","Unique ID / primary key for deployment."
   ".. _deployed_equipment:

   deployed_equipment","str","`master_data.equipment.id <../master_data/equipment.html#id>`_","Optional","The deployed equipment."
   ".. _host:

   host","str","`master_data.host.id <../master_data/host.html#id>`_","Optional","The host / observing facility where the equipment is deployed."
   ".. _height_above_local_reference_surface:

   height_above_local_reference_surface","float",,"Optional","Installation height of equipment above reference surface (in meters)."
   ".. _local_reference_surface:

   local_reference_surface","str","`reference_data.reference_surface.id <../reference_data/reference_surface.html#id>`_","Optional","The local reference surface."
   ".. _valid_from:

   valid_from","datetime",,"Optional","Date that this record is valid from."
   ".. _valid_to:

   valid_to","datetime",,"Optional","Date that this record is valid to."
   ".. _communication_method:

   communication_method","str","`reference_data.communication_method.id <../reference_data/communication_method.html#id>`_","Optional","The primary data communication method."
   ".. _source_of_observation:

   source_of_observation","str","`reference_data.source_of_observation.id <../reference_data/source_of_observation.html#id>`_","Required","The source of the observation (manual, automatic, visual etc.)."
   ".. _exposure:

   exposure","str","`reference_data.exposure.id <../reference_data/exposure.html#id>`_","Optional","The degree to which an instrument is affected by external influences according to the exposure classification (see WMO No. 8)."
   ".. _measurement_quality:

   measurement_quality","str","`reference_data.measurement_quality.id <../reference_data/measurement_quality.html#id>`_","Optional","Expected quality of measurements from the sensor in teh current configuration according to the measurement quality classification (see WMO-No. 8)."
   ".. _representativeness:

   representativeness","str","`reference_data.representativeness.id <../reference_data/representativeness.html#id>`_","Optional","An assessment of the representativeness of the observations."
   ".. _configuration:

   configuration","str",,"Optional","Description of any shielding or configuration/setup of the instrumentation."
   ".. _control_schedule:

   control_schedule","str",,"Optional","Description of schedule for calibrations or verification of instrument."
   ".. _maintenance_schedule:

   maintenance_schedule","str",,"Optional","A description (and schedule) of maintenance that is routinely performed on an instrument."
   ".. _links:

   links","dict",,"Optional","Link(s) to further information on deployment."
   ".. _version:

   _version","int",,"Required","Version number of this record."
   ".. _change_date:

   _change_date","datetime",,"Required","Date this record was changed."
   ".. _user:

   _user","str","`admin.user.id <../admin/user.html#id>`_","Required","Which user/agent last modified this record."
   ".. _status:

   _status","str","`reference_data.status.id <../reference_data/status.html#id>`_","Required","Whether this is the latest version or an archived version of the record."
   ".. _comments:

   _comments","str",,"Required","Free text comments on this record, for example description of changes made etc."

