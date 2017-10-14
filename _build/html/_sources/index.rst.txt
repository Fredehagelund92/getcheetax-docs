Cheetax - Exasol data loader
============================

Cheetax is a command-line interface to load data from various sources into Exasol.
Its primary audiance are data science that would like to get started quickly with a fully functional
datawarehouse.
|

For maximum performance and compatibility the commands are built upon native Exasol functionality
like the import statement and UDF. This ensures that everything is running in the acriss the cluster.
to learn more about how UDF and Import statement, please check out the
`Exasol documentation <https://www.exasol.com/support/secure/attachment/49848/EXASOL_User_Manual-6.0.0-en.pdf>`_.


Cheetax is free to use (`MIT license <https://github.com/Fredehagelund92/Cheetax/blob/master/LICENSE>`_),
open source (`GitHub <https://github.com/blue-yonder/turbodbc>`_),
available for Linux, OSX, and Windows.


Cheetax is routinely tested with loading data from JDBC (`MySQL <https://www.mysql.com>`_,
`PostgreSQL <https://www.postgresql.org>`_, `EXASOL <http://www.exasol.com>`_,
, `MSSQL <http://microsoft.com/sql>`_, `Oracle <http://www.oracle.com/technetwork/database/database-technologies/sql/overview/index.html>`_),
`CSV <https://en.wikipedia.org/wiki/Comma-separated_values>`_ and `JSON <http://www.json.org/>`_. However it will probably work with other JDBC connectors aswell.




.. toctree::
  :maxdepth: 1

  introduction
  getting_started
  guides
  reference
  version_history
  faq
