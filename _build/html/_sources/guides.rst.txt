.. autoclass:: guides
    :members:

Guides
======


Configuration
-------------

Profile
~~~~~~~~~~~~~

Cheetax is developed for Exasol and therefore you are not able to specify any database type.
Below is in example of an profile configuration file. You can also find examples by navigating to
``~/.cheetax/profiles``.

.. code-block:: yaml

  ---
  host: "127.0.0.1"
  port: 8563
  database: exa_db1
  username: root
  password: mypassword


Source
~~~~~~~~~~~~~

Cheetax support a number of different source types. Source information is
listed below.


**EXASOL**

.. code-block:: yaml

  ---
  type: exasol
  host:  "127.0.0.1"
  port: 8563
  user: root
  pass: mypassword
  database: exa_db1
  schema: customers
  schema_alias: cust
  table: account
  table_alias:
  primary_keys: ['id']
  select: 'id, name'
  where: "delete_flag = 0"


*   **type:** name of the source type (string, Available values options are: ``exasol``, ``oracle``, ``mssql``, ``postgresql``, ``mysql``, ``json``, ``csv``)
*   **host:** database host name (string, required)
*   **port:** database port number (integer, default: 8563)
*   **user:** database login user name (string, required)
*   **pass:** database login password (string, required)
*   **database:** database name (string, default: "")
*   **schema:** schema name (string, required)
*   **schema_alias:** if set, will be used instead of ``schema`` in datawarehouse (string, default: "")
*   **table:** table name (string, required)
*   **table_alias:** if set, will be used as part of ``table`` in datawarehouse (string, default: "")
*   **primary_keys:** column names of primary keys (array of strings, default: use primary keys)
*   **select:** expression of select (e.g. id, created_at) (string, default: "*")
*   **where:** where clause to filter the rows (string, default: no-condition)
*   **incremental:** if true, enables incremental loading. (boolean, default: false)
*   **incremental_columns:** column names for incremental loading (array of strings, default: use primary keys)
*   **last_record:** values of the last record for incremental loading (array of objects, default: load all records)


**MSSQL**

.. code-block:: yaml

  ---
  type: mysql
  host:  "127.0.0.1"
  port: 1433
  instance: test
  user: root
  pass: mypassword
  database: mssql_db1
  schema: customers
  schema_alias: cust
  table: account
  table_alias:
  primary_keys: ['id']
  select: 'id, name'
  where: "delete_flag = 0"


*   **type:** name of the source type (string, Available values options are: ``exasol``, ``oracle``, ``mssql``, ``postgresql``, ``mysql``, ``json``, ``csv``)
*   **host:** database host name (string, required)
*   **instance:** instance name. if instance is set, port option will be ignored (string, default: "")
*   **port:** database port number (integer, default: 1433)
*   **user:** database login user name (string, required)
*   **pass:** database login password (string, required)
*   **database:** database name (string, default: "")
*   **schema:** schema name (string, required)
*   **schema_alias:** if set, will be used instead of ``schema`` in datawarehouse (string, default: "")
*   **table:** table name (string, required)
*   **table_alias:** if set, will be used as part of ``table`` in datawarehouse (string, default: "")
*   **primary_keys:** column names of primary keys (array of strings, default: use primary keys)
*   **select:** expression of select (e.g. id, created_at) (string, default: "*")
*   **where:** where clause to filter the rows (string, default: no-condition)
*   **incremental:** if true, enables incremental loading. (boolean, default: false)
*   **incremental_columns:** column names for incremental loading (array of strings, default: use primary keys)
*   **last_record:** values of the last record for incremental loading (array of objects, default: load all records)



**POSTGRESQL**

.. code-block:: yaml

  ---
  type: mysql
  host:  "127.0.0.1"
  port: 5432
  user: root
  pass: mypassword
  database: post_db1
  schema: customers
  schema_alias: cust
  table: account
  table_alias:
  primary_keys: ['id']
  select: 'id, name'
  where: "delete_flag = 0"


*   **type:** name of the source type (string, Available values options are: ``exasol``, ``oracle``, ``mssql``, ``postgresql``, ``mysql``, ``json``, ``csv``)
*   **host:** database host name (string, required)
*   **port:** database port number (integer, default: 5432)
*   **user:** database login user name (string, required)
*   **pass:** database login password (string, required)
*   **database:** database name (string, default: "")
*   **schema:** schema name (string, required)
*   **schema_alias:** if set, will be used instead of ``schema`` in datawarehouse (string, default: "")
*   **table:** table name (string, required)
*   **table_alias:** if set, will be used as part of ``table`` in datawarehouse (string, default: "")
*   **primary_keys:** column names of primary keys (array of strings, default: use primary keys)
*   **select:** expression of select (e.g. id, created_at) (string, default: "*")
*   **where:** where clause to filter the rows (string, default: no-condition)
*   **incremental:** if true, enables incremental loading. (boolean, default: false)
*   **incremental_columns:** column names for incremental loading (array of strings, default: use primary keys)
*   **last_record:** values of the last record for incremental loading (array of objects, default: load all records)



**MYSQL**

.. code-block:: yaml

  ---
  type: mysql
  host:  "127.0.0.1"
  port: 3306
  user: root
  pass: mypassword
  database: mysql_db1
  schema: customers
  schema_alias: cust
  table: account
  table_alias:
  primary_keys: ['id']
  select: 'id, name'
  where: "delete_flag = 0"


*   **type:** name of the source type (string, Available values options are: ``exasol``, ``oracle``, ``mssql``, ``postgresql``, ``mysql``, ``json``, ``csv``)
*   **host:** database host name (string, required)
*   **port:** database port number (integer, default: 3306)
*   **user:** database login user name (string, required)
*   **pass:** database login password (string, required)
*   **database:** database name (string, default: "")
*   **schema:** schema name (string, required)
*   **schema_alias:** if set, will be used instead of ``schema`` in datawarehouse (string, default: "")
*   **table:** table name (string, required)
*   **table_alias:** if set, will be used as part of ``table`` in datawarehouse (string, default: "")
*   **primary_keys:** column names of primary keys (array of strings, default: use primary keys)
*   **select:** expression of select (e.g. id, created_at) (string, default: "*")
*   **where:** where clause to filter the rows (string, default: no-condition)
*   **incremental:** if true, enables incremental loading. (boolean, default: false)
*   **incremental_columns:** column names for incremental loading (array of strings, default: use primary keys)
*   **last_record:** values of the last record for incremental loading (array of objects, default: load all records)



**ORACLE**

.. code-block:: yaml

  ---
  type: oracle
  host:  "127.0.0.1"
  port: 1521
  user: root
  pass: mypassword
  database: exa_db1
  schema: customers
  schema_alias: cust
  table: account
  table_alias:
  primary_keys: ['id']
  select: 'id, name'
  where: "delete_flag = 0"


*   **type:** name of the source type (string, Available values options are: ``exasol``, ``oracle``, ``mssql``, ``postgresql``, ``mysql``, ``json``, ``csv``)
*   **host:** database host name (string, required)
*   **port:** database port number (integer, default: 1521)
*   **user:** database login user name (string, required)
*   **pass:** database login password (string, required)
*   **database:** database name (string, default: "")
*   **schema:** schema name (string, required)
*   **schema_alias:** if set, will be used instead of ``schema`` in datawarehouse (string, default: "")
*   **table:** table name (string, required)
*   **table_alias:** if set, will be used as part of ``table`` in datawarehouse (string, default: "")
*   **primary_keys:** column names of primary keys (array of strings, default: use primary keys)
*   **select:** expression of select (e.g. id, created_at) (string, default: "*")
*   **where:** where clause to filter the rows (string, default: no-condition)
*   **incremental:** if true, enables incremental loading. (boolean, default: false)
*   **incremental_columns:** column names for incremental loading (array of strings, default: use primary keys)
*   **last_record:** values of the last record for incremental loading (array of objects, default: load all records)


**CSV**

.. code-block:: yaml

  ---
  type: csv
  host: /Users/frederikhagelund/.cheetax/tmp
  path_to_file: files/exchange_rate.csv
  header_lines: True
  row_separator: 'CRLF'
  column_separator: ','
  columns:
      - {name: time, type: timestamp, format: "%Y-%m-%d"}
      - {name: name, type: string, max_length: 18}

*   **type:** name of the source type (string, Available values options are: ``exasol``, ``oracle``, ``mssql``, ``postgresql``, ``mysql``, ``json``, ``csv``)
*   **endpoint:** Server endpoint/url (string, Required. Example values are: ``https://testbucket.s3.amazonaws.com``, ``http://127.0.0.1``)
*   **path_to_file:** Path to the file  (string, Required)
*   **s3_key_id:** AWS access key ID (string, default: "")
*   **s3_secret_key:** AWS secret access key (string, default: "")
*   **row_separator:** row seperator (string, Example values are: ``CR``, ``LF``, ``CRLF``)
*   **columns:** advanced: a key-value pairs where key is a column name and value is options for the column.
  *   **name:** column name (string, default: "")
  *   **type:** sql data type (string, Available values options are: ``varchar``, ``double``, ``decimal``, ``boolean``, ``date``, ``timestamp`` and ``geometry``)
  *   **format:** date and timestamp format (string, Example values are ``YYYY-MM-DD``)
  *   **max_length:** maximum length for type (string, default: "")
  *   **precision:** precision for ``decimal`` type (string, default: "")
  *   **scale:** scale for ``decimal`` type (string, default: "")




**JSON**

.. code-block:: yaml

  ---
  type: json
  server: /Users/frederikhagelund/.cheetax/tmp
  file_name: exchange_rate.csv
  root_object_path: "$.account"
  row_separator: 'CRLF'
  column_separator: ','
  columns:
      - {name: time, type: timestamp, format: "%Y-%m-%d", object_path: timestamp}
      - {name: name, type: string, max_length: 18, object_path: name}



Testing
-------

Before loading data into your datawarehouse its a good idea to test the connection.

first test the connection to the profile

.. code-block:: shell

  cheetax connect --profile dev.yml

If the connection is successful you can start testing if the profile can connect to sources.

.. code-block:: shell

  cheetax test --profile-file dev.yml --source-file account.yml



Setup
-----

Before loading data into datawarehouse you need to setup schemas, tables and scripts.
This is done using ``setup`` command.

.. code-block:: shell

  cheetax setup --profile-file dev.yml --source-file account.yml



Load
----

Now you can insert data into your datawarehouse using ``load`` command.

.. code-block:: shell

  cheetax load --profile-file dev.yml --source-file account.yml
