.. autoclass:: introduction
    :members:

Introduction
============

Cheetax is a data loader command-line interface that helps transfer data between storages,
databases and files into EXASOL.
Cheetax is build around generic EXASOL import statements in order to maximize the performance of the load.

Features
--------

*   Automatically creation of tables and schemas
*   Bulk transfer using native import
*   Simple configuration using yaml syntax
*   Connection utility tester


Why use Cheetax?
----------------
Getting started with a datawarehouse can often be very time consuming process since you need to
create data pipelines from scratch. This is often done with either with a etl (talend, pentaho etc.)
or programming languages such as Python. Even though this creates a lot of freedom, it is also a
maintenance nightmare.

Is this proven? no however all i can say is based on my experience this is by far the easiest way to
maintenance a datawarehouse, where loading is done in batches.

Try it out and feedback through github is highly appreciated!



Supported OS
------------
Cheetax is developed in python, which means that it is compatible with following operations systems:

*   Windows
*   macOS
*   Ubuntu / Debian


Supported Databases
-------------------
We're currently only supporting Exasol 6.0 and above.

for information about supported source databases, view here.
