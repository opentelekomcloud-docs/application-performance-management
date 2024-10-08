:original_name: apm_01_0032.html

.. _apm_01_0032:

Threads
=======

This section describes the types, names, and meanings of thread metrics collected by APM.

.. table:: **Table 1** Thread collection parameters

   +-----------------------------+-----------+------------------+---------+-------------------------------+-----------------------------+-----------------------------------------------------------------------+
   | Parameter                   | Data Type | Application Type | Default | Supported Start Agent Version | Supported End Agent Version | Description                                                           |
   +=============================+===========+==================+=========+===============================+=============================+=======================================================================+
   | Max. Rows of Thread Details | integer   | JAVA             | 1       | 2.3.19                        | ``-``                       | Maximum number of rows of thread details. You can set it to up to 50. |
   +-----------------------------+-----------+------------------+---------+-------------------------------+-----------------------------+-----------------------------------------------------------------------+

.. table:: **Table 2** Thread metrics

   +-----------------------------------+------------+------------+-------------------+-------+-----------+--------------------------+
   | Category                          | Metric     | Name       | Description       | Unit  | Data Type | Default Aggregation Mode |
   +===================================+============+============+===================+=======+===========+==========================+
   | Thread details (**threadDetail**) | threadName | threadName | Thread name       | ``-`` | ENUM      | LAST                     |
   +-----------------------------------+------------+------------+-------------------+-------+-----------+--------------------------+
   |                                   | memory     | memory     | Memory            | ``-`` | INT       | SUM                      |
   +-----------------------------------+------------+------------+-------------------+-------+-----------+--------------------------+
   |                                   | stack      | stack      | Thread stack      | ``-`` | CLOB      | LAST                     |
   +-----------------------------------+------------+------------+-------------------+-------+-----------+--------------------------+
   |                                   | ids        | ids        | Thread ID         | ``-`` | STRING    | LAST                     |
   +-----------------------------------+------------+------------+-------------------+-------+-----------+--------------------------+
   |                                   | cpuTime    | cpuTime    | Thread CPU time   | ms    | INT       | SUM                      |
   +-----------------------------------+------------+------------+-------------------+-------+-----------+--------------------------+
   |                                   | count      | count      | Number of threads | ``-`` | INT       | LAST                     |
   +-----------------------------------+------------+------------+-------------------+-------+-----------+--------------------------+
