:original_name: apm_01_0055.html

.. _apm_01_0055:

CSEConsumer Cluster Monitoring
==============================

This section describes the types, names, and meanings of CSEConsumer cluster metrics collected by APM.

.. table:: **Table 1** CSEConsumer cluster metrics

   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   | Category                                                                                                                       | Metric        | Name          | Description                                           | Unit  | Data Type | Default Aggregation Mode |
   +================================================================================================================================+===============+===============+=======================================================+=======+===========+==========================+
   | CSEConsumer cluster monitoring (**cluster**: APM counts call statistics based on the ID of the cluster called by CSEConsumer.) | clusterId     | clusterId     | ID of the cluster where the called service is located | ``-`` | ENUM      | LAST                     |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | errorCount    | errorCount    | Number of errors                                      | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | invokeCount   | invokeCount   | Number of times the cluster is called                 | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | maxTime       | maxTime       | Maximum response time for calling the cluster         | ms    | INT       | MAX                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | totalTime     | totalTime     | Total response time for calling the cluster           | ms    | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   | CSEConsumer call details (**detail**: APM counts the call statistics based on the called URL.)                                 | qualifiedName | qualifiedName | CSEConsumer call URL                                  | ``-`` | ENUM      | LAST                     |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | method        | method        | HTTP method for CSEConsumer calling                   | ``-`` | ENUM      | LAST                     |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | concurrentMax | concurrentMax | Maximum number of concurrent CSEConsumer calls        | ``-`` | INT       | MAX                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | errorCount    | errorCount    | Number of CSEConsumer call errors                     | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | errorTraceId  | errorTraceId  | ID of the error trace in a collection period          | ``-`` | STRING    | LAST                     |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | slowTraceId   | slowTraceId   | ID of the slowest trace in a collection period        | ``-`` | STRING    | LAST                     |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | invokeCount   | invokeCount   | Number of CSEConsumer calls                           | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | lastError     | lastError     | Call error details                                    | ``-`` | STRING    | LAST                     |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | maxTime       | maxTime       | Maximum response time for CSEConsumer calling         | ms    | INT       | MAX                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | totalTime     | totalTime     | Total response time for CSEConsumer calling           | ms    | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | range1        | range1        | Number of requests with 0-10 ms response time         | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | range2        | range2        | Number of requests with 10-100 ms response time       | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | range3        | range3        | Number of requests with 100-500 ms response time      | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | range4        | range4        | Number of requests with 500-1000 ms response time     | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | range5        | range5        | Number of requests with 1-10s response time           | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | range6        | range6        | Number of requests with response time longer than 10s | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   | CSEConsumer summary (**total**: summary of CSEConsumer call statistics)                                                        | errorCount    | errorCount    | Total number of CSEConsumer call errors               | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | invokeCount   | invokeCount   | Total number of CSEConsumer calls                     | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
   |                                                                                                                                | totalTime     | totalTime     | Total response time for CSEConsumer calling           | ``-`` | INT       | SUM                      |
   +--------------------------------------------------------------------------------------------------------------------------------+---------------+---------------+-------------------------------------------------------+-------+-----------+--------------------------+
