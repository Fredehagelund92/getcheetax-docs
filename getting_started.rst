.. autoclass:: getting_started
    :members:

Getting Started
===============

Installation
------------

Linux and OSX
~~~~~~~~~~~~~

First, make sure you have python-dev installed:

.. code-block:: shell

  sudo apt-get install python-dev

then install using pip

.. code-block:: shell

  pip install cheetax

To upgrade, use:

.. code-block:: shell

  pip install --upgrade cheetax

macOS
~~~~~~~~~~~~~

To install cheetax it is recommended to `pip`

.. code-block:: shell

  pip install cheetax

To upgrade, use:

.. code-block:: shell

  pip install --upgrade cheetax


Windows
~~~~~~~~~~~~~

Before starting, you'll need to install
`Python version 3.5 or higher for Windows <https://www.python.org/downloads/windows/>`_.

Open up Windows powershell as an administrator, and with pip:

.. code-block:: shell

  pip install cheetax

To upgrade, use:

.. code-block:: shell

  pip install --upgrade cheetax


Create project
--------------

To create your first cheetax project, run:

.. code-block:: shell

  cheetax init

This will create a directory at `./.cheetax` with almost everything you need to get started.

Inside the `./cheetax` there will be two directories named `./profiles` and `./sources`. These directories
contains files that are responsible for defining data that should be loaded and where it should be stored.

.. warning::

  Remember configuration files contains sensitive information in terms of database credentials.
  this means that security is handled by the OS folder structure.

Locate project
--------------

To locate your project run

To create your first cheetax project, run:

.. code-block:: shell

  cheetax debug --config-dir
