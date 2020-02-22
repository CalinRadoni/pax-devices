===============================================================================
Development of this documentation
===============================================================================

This documentation is created with `Sphinx <https://www.sphinx-doc.org>`_ .

In Debian install :samp:`Sphinx` with ``sudo apt install python3-sphinx`` .

Project configuration
-------------------------------------------------------------------------------

In the project's directory create the :file:`docs` directory and run the
:command:`sphinx-quickstart` command inside that directory:

.. code-block:: bash

    mkdir docs
    cd docs
    sphinx-quickstart

Except for project's **name**, **author** and **version** I din not changed implicit values.

Read the Docs Sphinx Theme
-------------------------------------------------------------------------------

To add the `Read the Docs Sphinx Theme <https://github.com/readthedocs/sphinx_rtd_theme>`_
go to the :file:`docs` directory and run these commands:

.. code-block:: bash

    mkdir /tmp/sphinx-rtd
    git clone https://github.com/readthedocs/sphinx_rtd_theme.git /tmp/sphinx-rtd
    cp -r /tmp/sphinx-rtd/sphinx_rtd_theme _themes/sphinx_rtd_theme
    rm -rf /tmp/sphinx-rtd

to download it and copy the theme inside this project's :file:`_themes` directory.

To use the theme edit the :file:`conf.py` to replace default theme:

.. code-block:: ini

    html_theme = 'alabaster'

with the new one:

.. code-block:: ini

    html_theme = 'sphinx_rtd_theme'
    html_theme_path = ['_themes', ]

See `sphinx_rtd_theme <https://github.com/readthedocs/sphinx_rtd_theme>`_ for it's license.

Building from terminal
-------------------------------------------------------------------------------

To build it run :command:`make html` in project's :file:`docs` directory.

Building from Visual Studio code
-------------------------------------------------------------------------------

In project's root directory create the :file:`.vscode/tasks.json` file with the following content:

.. code-block:: json

    {
        "version": "2.0.0",
        "linux": {
            "type": "shell",
            "options": {
                "cwd": "${workspaceFolder}"
            },
            "presentation": {
                "echo": true,
                "reveal": "always",
                "focus": true,
                "panel": "shared",
                "showReuseMessage": false,
                "clear": false
            },
        },
        "problemMatcher": [],
        "tasks": [
            {
                "label": "Build HTML",
                "command": "make",
                "args": [ "html" ],
                "group": "build",
                "options": {
                    "cwd": "${workspaceFolder}/docs"
                }
            }
        ]
    }

To create HTML files use :kbd:`Control-Shift-B` and select :menuselection:`Build HTML pax-devices` option.
