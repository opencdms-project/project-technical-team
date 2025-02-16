:html_theme.sidebar_secondary.remove:

host_location
====

Download the definition as a CSV file: :download:`csv <host_location.csv>`.

.. csv-table:: Definition of the *host_location* table.
   :header: "Property","Kind","References","Requirement","Description"

   ".. _id:

   id","str",,"Required","Primary key for this record."
   ".. _host:

   host","str","`master_data.host.id <../master_data/host.html#id>`_","Required","Host/station associated with this record."
   ".. _location:

   location","Geography",,"Optional","Location of host/station during indicated time period."
   ".. _elevation:

   elevation","float",,"Optional","Elevation of station above mean sea level in meters."
   ".. _geopositioning_method:

   geopositioning_method","str","`reference_data.geopositioning_method.id <../reference_data/geopositioning_method.html#id>`_","Optional","Method by which the location was determined"
   ".. _valid_from:

   valid_from","datetime",,"Optional","Date from which the details for this record are valid."
   ".. _valid_to:

   valid_to","datetime",,"Optional","Date after which the details for this record are no longer valid."
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

