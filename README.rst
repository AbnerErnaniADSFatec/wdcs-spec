..
    This file is part of Web Data Cube Service Specification.
    Copyright (C) 2019 INPE.

    Web Data Cube Service Specification is free software; you can redistribute it and/or modify it
    under the terms of the MIT License; see LICENSE file for more details.


=====================================
Web Data Cube Service - Specification
=====================================

.. image:: https://img.shields.io/badge/license-MIT-green
        :target: https://github.com/brazil-data-cube/wdcs-spec/blob/master/LICENSE
        :alt: Software License

.. image:: https://img.shields.io/badge/lifecycle-experimental-orange.svg
        :target: https://www.tidyverse.org/lifecycle/#experimental
        :alt: Software Life Cycle

.. image:: https://img.shields.io/github/tag/brazil-data-cube/wdcs-spec.svg
        :target: https://github.com/brazil-data-cube/wdcs-spec/releases
        :alt: Release

.. image:: https://badges.gitter.im/brazil-data-cube/community.png
        :target: https://gitter.im/brazil-data-cube/community#
        :alt: Join the chat


About
=====

The **W**\ eb **D**\ ata **C**\ ube **S**\ ervice (WDCS) provides an interface to access slices of Earth observation data cubes from a `STAC service <https://github.com/radiantearth/stac-spec>`_. The three operations offered by the service are:

- ``list_cubes``: List all available data cubes from a given WDCS.

- ``describe_cube``: Provides a JSON document with the associated metadata of a data cube.

- ``get_cube``: Retrieves the list of assets ordered in space and time.


There are free and open source implementations based on this specification:

- `wdcs-server <https://github.com/brazil-data-cube/wdcs-server>`_: is a WDCS web server implemented in Python.

- `wdcs <https://github.com/brazil-data-cube/wdcs.R>`_: is a client API for R.


Repository Organization
-----------------------

- `api <./api>`_: WDCS Specification using OpenAPI 3.0.

- `jsonschemas <./jsonschemas>`_: `JSON Schema <https://json-schema.org/>`_ for WDCS responses.


Building the Documentation
==========================

Requirements
------------

The build system for the REST API documentation relies on the Node.js run-time environment:


  - `Node.js <https://nodejs.org/en/>`_ (Version 8+).
  - `ReDoc <https://github.com/Redocly/redoc>`_: generates HTML reference documentation from an OpenAPI specification file.


Build
-----

If you have Node.js installed, please, execute the following command to install the ReDoc dependency:

.. code-block:: shell

    $ npm install

After that, generate the documentation:

.. code-block:: shell

    $ npm run build

The above command will create a folder named ``dist`` with the bundled file index.html. You may open it in your web browser or may serve it with an HTTP Server.

For Python developers, you can serve the HTMl with:

.. code-block:: shell

        python3.7 -m http.server 8080 --directory dist


License
=======

.. admonition::
    Copyright (C) 2019 INPE.

    Web Data Cube Service is free software; you can redistribute it and/or modify it
    under the terms of the MIT License; see LICENSE file for more details.