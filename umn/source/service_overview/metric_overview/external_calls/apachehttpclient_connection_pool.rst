:original_name: apm_01_0054.html

.. _apm_01_0054:

ApacheHttpClient Connection Pool
================================

This section describes the types, names, and meanings of ApacheHttpClient connection pool metrics collected by APM.

.. table:: **Table 1** ApacheHttpClient connection pool metrics

   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   | Category                                                                                                | Metric    | Name      | Description                                          | Unit  | Data Type | Default Aggregation Mode |
   +=========================================================================================================+===========+===========+======================================================+=======+===========+==========================+
   | Connection pool (**connectionPool**: statistics about ApacheHttpclient connections in different states) | poolId    | poolId    | ApacheHttpclient connection pool ID                  | ``-`` | ENUM      | LAST                     |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | available | available | Number of idle connections in the connection pool    | ``-`` | INT       | SUM                      |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | leased    | leased    | Number of connections occupied                       | ``-`` | INT       | SUM                      |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | max       | max       | Maximum number of connections in the connection pool | ``-`` | INT       | MAX                      |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | pending   | pending   | Number of pending connections in the connection pool | ``-`` | INT       | SUM                      |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   | Connection pool route (**collectionPoolRoute**: APM counts connection statistics by pool route.)        | poolId    | poolId    | ApacheHttpClient connection pool ID                  | ``-`` | ENUM      | LAST                     |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | route     | route     | Routing information of the connection pool           | ``-`` | ENUM      | LAST                     |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | available | available | Number of idle connections in the connection pool    | ``-`` | INT       | SUM                      |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | leased    | leased    | Number of connections occupied                       | ``-`` | INT       | SUM                      |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | max       | max       | Maximum number of connections in the connection pool | ``-`` | INT       | MAX                      |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                         | pending   | pending   | Number of pending connections in the connection pool | ``-`` | INT       | SUM                      |
   +---------------------------------------------------------------------------------------------------------+-----------+-----------+------------------------------------------------------+-------+-----------+--------------------------+
