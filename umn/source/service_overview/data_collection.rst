:original_name: apm_01_0009.html

.. _apm_01_0009:

Data Collection
===============

After you enable data collection, APM collects application performance metrics and tracing data. Your personal privacy data will not be collected. The collected data will be used only for application performance analysis and fault diagnosis, and will not be used for commercial purposes.

+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+---------------------------------------------+----------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Data Type               | Collected Data                                                                                                                                                                                                              | Transmission Mode      | Storage Mode                                | Function                                           | Storage Period                                                                                                             |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+---------------------------------------------+----------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Performance metric data | JVM data, exceptions, databases, SQL statements, and middleware call data                                                                                                                                                   | WebSocket Secure (WSS) | Tenant-based isolated storage on the server | Metric query and display at the frontend           | 7 days for the basic edition and 30 days for the enterprise edition. The data will be permanently deleted upon expiration. |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+---------------------------------------------+----------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Tracing data            | Trace event data, including middleware invocation data                                                                                                                                                                      | WSS                    | Tenant-based isolated storage on the server | Query and display at the tracing frontend          | 7 days for the basic edition and 30 days for the enterprise edition. The data will be permanently deleted upon expiration. |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+---------------------------------------------+----------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Resource information    | Service type, service name, creation time, deletion time, node address, and service release API                                                                                                                             | WSS                    | Tenant-based isolated storage on the server | Query and display at the resource library frontend | 7 days for the basic edition and 30 days for the enterprise edition. The data will be permanently deleted upon expiration. |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+---------------------------------------------+----------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+
| Resource attributes     | System type, system startup event, number of CPUs, service executor, service process ID, service pod ID, CPU label, system version, web framework, JVM version, time zone, system name, collector version, and LastMail URL | WSS                    | Tenant-based isolated storage on the server | Query and display at the resource library frontend | 7 days for the basic edition and 30 days for the enterprise edition. The data will be permanently deleted upon expiration. |
+-------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+------------------------+---------------------------------------------+----------------------------------------------------+----------------------------------------------------------------------------------------------------------------------------+

.. table:: **Table 1** Restrictions on collection items

   ==================================================== ===============
   Collection Item                                      Maximum Value
   ==================================================== ===============
   Monitoring item rows                                 500
   SQL length                                           2000 characters
   SQL result bodies                                    100
   SQL result body content                              999 characters
   Redis body length                                    100 characters
   Mongo clusters                                       10
   Mongo command length                                 2000 characters
   HBase command length                                 500 characters
   ES RestClients                                       10
   Cassandra CQL length                                 2000 characters
   Cassandra sessions                                   10
   Kafka MBean object names                             100
   Cache IP addresses corresponding to Kafka client IDs 100
   RabbitMQ connection addresses                        20
   Cache connections for each RabbitMQ address          100
   RabbitMQ consumers                                   500
   Cache channels for each RabbitMQ consumer            100
   RabbitMQ messages without ACK in each channel        3000
   Manual ACK consumers in RabbitMQ cache               20
   RocketMQ PIDs                                        20
   RocketMQ client IDs                                  20
   Jetcd tag length                                     500 characters
   HttpClient connections                               10
   Report time of connection pool trace                 1 ms
   Dubbo invocation length                              500 characters
   Dubbo attachment length                              500 characters
   URL body length                                      9999 characters
   Application code body length                         0 characters
   Java method body length                              8192 characters
   ==================================================== ===============
