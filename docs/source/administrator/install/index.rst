Installation
============

OpenCDMS is not yet ready for production use. The instructions below give details on how to install a demo version of the software locally using docker containers.

Prerequisites
~~~~~~~~~~~~~
- git
- docker
- python 3


OpenCDMS database and API
~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: shell
    
    git clone https://github.com/opencdms/opencdms
    cd opencdms/install

    # If required, build the containers from scratch
    docker compose build --no-cache database api

    # start the database and api containers
    docker compose up database api --detach

The OpenCDMS API is now accessible locally at http://localhost:5000. Furthermore, you can connect to the Postgress database using the details in `install/default.env`.

Build database
~~~~~~~~~~~~~~

.. code-block:: shell

    # Build database from api container
    docker exec -it opencdms-api bash

    git clone https://github.com/opencdms/opencdms-test-data /local/opencdms-test-data --depth 1

    cd /local/app/opencdms/install
    python3 initialise_database.py
    python3 ingest_code_tables.py
    python3 ingest_sample_data.py 


Install OpenCDMS App
~~~~~~~~~~~~~~~~~~~~

.. code-block:: shell
    
    git clone https://github.com/opencdms/opencdms-app
    docker compose up app --detach


OpenCDMS App is now accessible locally at http://localhost:8000. The app will connect to the local API instance that was installed at http://localhost:5000.
