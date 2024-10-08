:original_name: apm_01_0027.html

.. _apm_01_0027:

GC Monitoring
=============

This section describes the types, names, and meanings of GC metrics collected by APM.

.. table:: **Table 1** GC metrics

   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   | Category                  | Metric            | Name              | Description                                     | Unit  | Data Type | Default Aggregation Mode |
   +===========================+===================+===================+=================================================+=======+===========+==========================+
   | GC statistics (**gc**)    | fullGCCount       | fullGCCount       | Number of full GC times in a collection period  | ``-`` | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | fullGCCountTotal  | fullGCCountTotal  | Total number of full GC times                   | ``-`` | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | fullGCTime        | fullGCTime        | Full GC duration in a collection period         | ms    | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | fullGCTimeTotal   | fullGCTimeTotal   | Total full GC duration                          | ms    | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | fullGCMBeanName   | fullGCMBeanName   | Name of the full GC recycler                    | ``-`` | STRING    | LAST                     |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | youngGCCount      | youngGCCount      | Number of young GC times in a collection period | ``-`` | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | youngGCCountTotal | youngGCCountTotal | Total number of young GC times                  | ``-`` | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | youngGCTime       | youngGCTime       | Young GC duration in a collection period        | ms    | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | youngGCTimeTotal  | youngGCTimeTotal  | Total young GC duration                         | ms    | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | youngGCMBeanName  | youngGCMBeanName  | Name of the young GC recycler                   | ``-`` | STRING    | LAST                     |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   | GC details (**gcdetail**) | action            | action            | GC type, which can be **major** or **minor**    | ``-`` | ENUM      | LAST                     |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | cause             | cause             | GC cause                                        | ``-`` | ENUM      | LAST                     |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | name              | name              | GC collector name                               | ``-`` | STRING    | LAST                     |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | count             | count             | Number of times that GC has occurred            | ``-`` | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | totalTime         | totalTime         | GC duration                                     | ms    | INT       | SUM                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | maxTime           | maxTime           | Time consumed by the slowest GC                 | ms    | INT       | MAX                      |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
   |                           | detail            | detail            | Details about the slowest GC                    | ``-`` | CLOB      | LAST                     |
   +---------------------------+-------------------+-------------------+-------------------------------------------------+-------+-----------+--------------------------+
