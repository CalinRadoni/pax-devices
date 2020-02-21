===============================================================================
Development
===============================================================================

This document specifies the development configuration ESP32 based pax-devices

Compiling with esp-idf
-------------------------------------------------------------------------------

I am compiling in Linux, Debian 10 to be precise.

Locations for code and application
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* ESP-IDF is installed in the default path, :file:`~/esp/esp-idf` .
* The :samp:`pax-devices` project is in the :file:`{CFG_Projects_Path}` directory
* The Visual Studio Code workspace is saved with the name :file:`{CFG_Projects_Path}/pax-devices/pax-devices.code-workspace`
* Additional ESP-IDF components are in :file:`{CFG_CodeLib_Path}/ESP32` and :file:`{CFG_CodeLib_Path}/Generic` directories

Create the :file:`~/vscode-pax-devices` with the following content:

.. code-block:: bash

    #!/bin/bash

    ProjectPath="CFG_Projects_Path/pax-devices"
    ProjectName="pax-devices"

    export CodeLib_PATH=CFG_CodeLib_Path

    cd $ProjectPath
    . ~/esp/esp-idf/export.sh
    code $ProjectPath/$ProjectName.code-workspace

Source that file with :command:`. vscode-pax-devices` and it will launch Visual Studio Code and a terminal.
From **that** terminal, to compile, flash and test (for example ``pax-Gateway``), use:

.. code-block:: bash

    cd CFG_Projects_Path/pax-Gateway/SW
    idf.py menuconfig
    idf.py build
    idf.py flash
    idf.py monitor

Example directory structure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* ESP-IDF is installed in the default path, :file:`~/esp/esp-idf` .
* The :samp:`pax-devices` project is in the :file:`/data/Projects/pax-devices` directory
* The Visual Studio Code workspace is saved with the name :file:`{CFG_Projects_Path}/pax-devices/pax-devices.code-workspace`
* Additional ESP-IDF components are in :file:`/data/Projects/CodeLibrary` directories:
    * :file:`Debouncer` is located in :file:`/data/Projects/CodeLibrary/Generic`
    * :file:`ESP32DLEDController`, :file:`ESP32RMT`, ... esp-idf components are located in :file:`/data/Projects/CodeLibrary/ESP32`

The :file:`/data/Projects/pax-devices/pax-devices.code-workspace` file is:

.. code-block:: json

    {
        "folders": [
            {
                "path": "."
            },
            {
                "path": "/data/Projects/pax-Gateway"
            },
            {
                "path": "/data/Projects/pax-DLED"
            },
            {
                "path": "/data/Projects/pax-DLEDGrid"
            },
            {
                "path": "/data/Projects/CodeLibrary"
            }
        ],
        "extensions": {
            "recommendations": [
                "ms-vscode.cpptools",
                "editorconfig.editorconfig",
                "tht13.rst-vscode",
                "ms-python.python",
                "gruntfuggly.todo-tree"
            ]
        }
    }

The :file:`vscode-pax-devices` file is:

.. code-block:: bash

    #!/bin/bash

    ProjectPath="/data/Projects/pax-devices"
    ProjectName="pax-devices"

    export CodeLib_PATH=/data/Projects/CodeLibrary

    cd $ProjectPath
    . ~/esp/esp-idf/export.sh
    code $ProjectPath/$ProjectName.code-workspace
