:original_name: apm_01_0057.html

.. _apm_01_0057:

Redis Method Call
=================

This section describes the types, names, and meanings of Redis method call metrics collected by APM.

.. table:: **Table 1** Redis method call collection parameters

   +----------------------+-----------+------------------+---------+-------------------------------+-----------------------------+-----------------------------------------------------+
   | Parameter            | Data Type | Application Type | Default | Supported Start Agent Version | Supported End Agent Version | Description                                         |
   +======================+===========+==================+=========+===============================+=============================+=====================================================+
   | Parameter Parsing    | radio     | JAVA             | false   | 2.0.0                         | ``-``                       | Whether to parse Redis parameters and return values |
   +----------------------+-----------+------------------+---------+-------------------------------+-----------------------------+-----------------------------------------------------+
   | Length               | integer   | JAVA             | 1000    | 2.0.0                         | ``-``                       | Maximum length of parameters to be parsed           |
   +----------------------+-----------+------------------+---------+-------------------------------+-----------------------------+-----------------------------------------------------+
   | Port Differentiation | radio     | JAVA             | false   | 2.0.0                         | ``-``                       | Whether to distinguish Redis ports                  |
   +----------------------+-----------+------------------+---------+-------------------------------+-----------------------------+-----------------------------------------------------+

.. table:: **Table 2** Call metrics

   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   | Name                        | Metric         | Name           | Description                                                                       | Unit  | Data Type | Default Aggregation Mode |
   +=============================+================+================+===================================================================================+=======+===========+==========================+
   | Call details (**detail**)   | host           | host           | Host                                                                              | ``-`` | ENUM      | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | action         | action         | Method                                                                            | ``-`` | ENUM      | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | lastError      | lastError      | Error message                                                                     | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | slowTraceId    | slowTraceId    | Slowest trace ID                                                                  | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | errorTraceId   | errorTraceId   | Error trace ID                                                                    | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range1         | range1         | Number of requests with 0-5 ms response time                                      | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range2         | range2         | Number of requests with 5-10 ms response time                                     | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range3         | range3         | Number of requests with 10-50 ms response time                                    | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range4         | range4         | Number of requests with 50-100 ms response time                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range5         | range5         | Number of requests with 100-1000 ms response time                                 | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range6         | range6         | Number of requests with response time longer than 1s                              | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | invokeCount    | invokeCount    | Number of calls                                                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | hits           | hits           | Hits of methods including GET, HGET, and EXPIRE                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | totalTime      | totalTime      | Total response time                                                               | ms    | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | maxTime        | maxTime        | Maximum response time                                                             | ms    | INT       | MAX                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | errorCount     | errorCount     | Number of errors                                                                  | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | runningCount   | runningCount   | Number of tasks that are being executed                                           | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | concurrentMax  | concurrentMax  | Maximum concurrency                                                               | ``-`` | INT       | MAX                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | blobCount      | blobCount      | Number of calls with more than 1000 bytes returned                                | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | getInvokeCount | getInvokeCount | Number of times that GET methods including GET, HGET, and EXPIRE have been called | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | traffic        | traffic        | Call traffic                                                                      | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   | Host summary (**host**)     | host           | host           | Host                                                                              | ``-`` | ENUM      | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | lastError      | lastError      | Error message                                                                     | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | slowTraceId    | slowTraceId    | Slowest trace ID                                                                  | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | errorTraceId   | errorTraceId   | Error trace ID                                                                    | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range1         | range1         | Number of requests with 0-5 ms response time                                      | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range2         | range2         | Number of requests with 5-10 ms response time                                     | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range3         | range3         | Number of requests with 10-50 ms response time                                    | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range4         | range4         | Number of requests with 50-100 ms response time                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range5         | range5         | Number of requests with 100-1000 ms response time                                 | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range6         | range6         | Number of requests with response time longer than 1s                              | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | invokeCount    | invokeCount    | Number of calls                                                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | hits           | hits           | Hits of methods including GET, HGET, and EXPIRE                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | totalTime      | totalTime      | Total response time                                                               | ms    | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | maxTime        | maxTime        | Maximum response time                                                             | ms    | INT       | MAX                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | errorCount     | errorCount     | Number of errors                                                                  | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | runningCount   | runningCount   | Number of tasks that are being executed                                           | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | blobCount      | blobCount      | Number of calls with more than 1000 bytes returned                                | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | getInvokeCount | getInvokeCount | Number of times that GET methods including GET, HGET, and EXPIRE have been called | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | traffic        | traffic        | Call traffic                                                                      | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   | Method summary (**action**) | action         | action         | Method                                                                            | ``-`` | ENUM      | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | lastError      | lastError      | Last exception type                                                               | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | slowTraceId    | slowTraceId    | Slowest trace ID                                                                  | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | errorTraceId   | errorTraceId   | Error trace ID                                                                    | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range1         | range1         | Number of requests with 0-5 ms response time                                      | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range2         | range2         | Number of requests with 5-10 ms response time                                     | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range3         | range3         | Number of requests with 10-50 ms response time                                    | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range4         | range4         | Number of requests with 50-100 ms response time                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range5         | range5         | Number of requests with 100-1000 ms response time                                 | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range6         | range6         | Number of requests with response time longer than 1s                              | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | invokeCount    | invokeCount    | Number of calls                                                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | hits           | hits           | Hits of methods including GET, HGET, and EXPIRE                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | totalTime      | totalTime      | Total response time                                                               | ms    | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | maxTime        | maxTime        | Maximum response time                                                             | ms    | INT       | MAX                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | errorCount     | errorCount     | Number of errors                                                                  | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | runningCount   | runningCount   | Ongoing executions                                                                | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | blobCount      | blobCount      | Number of calls with more than 1000 bytes returned                                | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | getInvokeCount | getInvokeCount | Number of times that GET methods including GET, HGET, and EXPIRE have been called | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | traffic        | traffic        | Traffic                                                                           | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   | Summary (**total**)         | lastError      | lastError      | Last exception type                                                               | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | slowTraceId    | slowTraceId    | Slowest trace ID                                                                  | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | errorTraceId   | errorTraceId   | Error trace ID                                                                    | ``-`` | STRING    | LAST                     |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range1         | range1         | Number of requests with 0-5 ms response time                                      | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range2         | range2         | Number of requests with 5-10 ms response time                                     | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range3         | range3         | Number of requests with 10-50 ms response time                                    | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range4         | range4         | Number of requests with 50-100 ms response time                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range5         | range5         | Number of requests with 100-1000 ms response time                                 | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | range6         | range6         | Number of requests with response time longer than 1s                              | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | invokeCount    | invokeCount    | Number of calls                                                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | hits           | hits           | Hits of methods including GET, HGET, and EXPIRE                                   | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | totalTime      | totalTime      | Total response time                                                               | ms    | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | maxTime        | maxTime        | Maximum response time                                                             | ms    | INT       | MAX                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | errorCount     | errorCount     | Number of errors                                                                  | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | runningCount   | runningCount   | Number of tasks that are being executed                                           | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | blobCount      | blobCount      | Number of calls with more than 1000 bytes returned                                | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | getInvokeCount | getInvokeCount | Number of times that GET methods including GET, HGET, and EXPIRE have been called | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
   |                             | traffic        | traffic        | Traffic                                                                           | ``-`` | INT       | SUM                      |
   +-----------------------------+----------------+----------------+-----------------------------------------------------------------------------------+-------+-----------+--------------------------+
