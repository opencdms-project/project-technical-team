:html_theme.sidebar_secondary.remove:

media_type
====

Media type code list.


.. raw:: html

   <style>

      /*disable page width for wide tables*/
      .bd-page-width {max-width: none;}
      .bd-article-container {max-width: 100% !important;}

      /* Limit primary side bar width for wide pages */
      .bd-sidebar-primary {max-width: 400px;}

      .sphinx-tabs-panel {overflow-x: scroll;}

   </style>

.. tabs::
    .. tab:: Table definition

        Download the definition as a CSV file: :download:`csv <media_type.csv>`.

        .. csv-table:: Definition of the *media_type* table.
           :header: "Property","Kind","References","Requirement","Description"

           ".. _id:

           id","str",,"Required","ID / primary key."
           ".. _inScheme:

           inScheme","str",,"Required","The scheme/vocabulary that this record is from."
           ".. _name:

           name","str",,"Required","Short name / abbreviation for the media type."
           ".. _description:

           description","str",,"Required","Description of the media type."
           ".. _links:

           links","dict",,"Optional","Link(s) to definition of media type."
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

    .. tab:: Example data

        Download the example CSV file: :download:`csv <./examples/media_type.csv>`.

        .. csv-table:: Example data
           :file: ./examples/media_type.csv
           :header-rows: 1
           :quote: '
