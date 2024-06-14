:original_name: apm_07_0010.html

.. _apm_07_0010:

SQL
===

This function monitors database access. The databases that can be monitored include the C3P0, Cassandra, ClickHouse, DBCP, Druid, EsRestClient, GaussDB, Hikari, Jetcd, ObsClient, MySQL, PostgreSQL, Oracle, HBase, and MongoDB. APM collects details about executed statements to help you locate performance problems in code.

This section focuses on MySQL database monitoring.

Going to the SQL Page
---------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Management & Deployment** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click |image2| next to the target environment.

#. Click the **SQL** tab. By default, the MySQL database information of all instances is displayed.


   .. figure:: /_static/images/en-us_image_0000001675948477.png
      :alt: **Figure 1** Going to the SQL page

      **Figure 1** Going to the SQL page

#. On the displayed **SQL** tab page, select a target instance and monitoring item to view the monitoring data in different metric sets.


   .. figure:: /_static/images/en-us_image_0000001627430564.png
      :alt: **Figure 2** Selecting an instance and monitoring item

      **Figure 2** Selecting an instance and monitoring item

#. Select a time range. Default: **Last 20 minutes**.

   Options: **Last 20 minutes**, **Last hour**, **Last 3 hours**, **Last 6 hours**, **Last day**, **Today**, **Yesterday**, **Last week**, **Last month**, or **Custom**.


   .. figure:: /_static/images/en-us_image_0000001602510794.png
      :alt: **Figure 3** Selecting a time range

      **Figure 3** Selecting a time range

#. Click |image3| in the upper right corner of the list and select the metric data you want to view.

Viewing MySQL Database Monitoring Data
--------------------------------------

**SQL summary**

APM can monitor MySQL databases by SQL. For details about the metrics, see :ref:`Table 1 <apm_07_0010__en-us_topic_0000001217564316_table835410610214>`. Click |image4| in the upper right corner of the list and select the metric data you want to view.


.. figure:: /_static/images/en-us_image_0000001627751380.png
   :alt: **Figure 4** SQL summary under MySQL database monitoring

   **Figure 4** SQL summary under MySQL database monitoring

.. _apm_07_0010__en-us_topic_0000001217564316_table835410610214:

.. table:: **Table 1** SQL summary parameters

   +----------------+-----------------+-----------------------------------------------------------------------+
   | Metric Set     | Metric          | Description                                                           |
   +================+=================+=======================================================================+
   | SQL monitoring | sql             | Unique ID of the SQL statement, which is used for alarm configuration |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | SQL Statement   | SQL statement                                                         |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Calls           | Number of times that the SQL statement is called                      |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Avg RT (ms)     | Average response time (ms)                                            |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Errors          | Number of errors that the SQL statement encounters                    |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Rows Read       | Number of read rows of the SQL statement                              |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Rows Updated    | Number of updated rows of the SQL statement                           |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Max Concurrency | Maximum concurrency of the SQL statement                              |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Max RT (ms)     | Maximum response time of the SQL statement                            |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | 0 ms-10 ms      | Number of requests with 0 ms-10 ms response time                      |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | 10 ms-100 ms    | Number of requests with 10 ms-100 ms response time                    |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | 100 ms-200 ms   | Number of requests with 100 ms-200 ms response time                   |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | 200 ms-1s       | Number of requests with 200 ms-1s response time                       |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | 1s-10s          | Number of requests with 1s-10s response time                          |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | 10s-n           | Number of requests with response time longer than 10s                 |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Slowest Trace   | ID of the slowest trace in a collection period                        |
   +----------------+-----------------+-----------------------------------------------------------------------+
   |                | Error Trace     | ID of the trace that encounters an error in a collection period       |
   +----------------+-----------------+-----------------------------------------------------------------------+

-  Click an SQL statement to view details.
-  Click a number in blue (such as those in the **Calls** or **Avg RT (ms)** column) to view more details.
-  Click a slow or an error trace to view its details.

**Database summary**

APM can summarize MySQL database metrics by database. For details about the metrics, see :ref:`Table 2 <apm_07_0010__en-us_topic_0000001217564316_table17186112310356>`.


.. figure:: /_static/images/en-us_image_0000001676071449.png
   :alt: **Figure 5** Database summary under MySQL database monitoring

   **Figure 5** Database summary under MySQL database monitoring

.. _apm_07_0010__en-us_topic_0000001217564316_table17186112310356:

.. table:: **Table 2** Database summary parameters

   +----------------------+-----------------------+---------------------------------------------------------------+
   | Metric Set           | Metric                | Description                                                   |
   +======================+=======================+===============================================================+
   | Database connections | db                    | Database name                                                 |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | Connections Created   | Number of connections created by the database                 |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | Connections Destroyed | Number of the database's connections that have been destroyed |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | Avg RT (ms)           | Average response time (ms)                                    |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | Calls                 | Number of times that the database is called                   |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | Errors                | Number of errors that the database encounters                 |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | Rows Read             | Number of rows read from the database                         |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | Rows Updated          | Number of rows updated in the database                        |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | Max RT (ms)           | Maximum response time of the database                         |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | 0 ms-10 ms            | Number of requests with 0 ms-10 ms response time              |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | 10 ms-100 ms          | Number of requests with 10 ms-100 ms response time            |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | 100 ms-200 ms         | Number of requests with 100 ms-200 ms response time           |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | 200 ms-1s             | Number of requests with 200 ms-1s response time               |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | 1s-10s                | Number of requests with 1s-10s response time                  |
   +----------------------+-----------------------+---------------------------------------------------------------+
   |                      | 10s-n                 | Number of requests with response time longer than 10s         |
   +----------------------+-----------------------+---------------------------------------------------------------+

Click a number in blue (such as those in the **Calls** or **Avg RT (ms)** column) to view more details.

**Exception**

On the **Exception** tab page, view exception statistics about SQL calls. For details about the metrics, see :ref:`Table 3 <apm_07_0010__en-us_topic_0000001217564316_table16208113154714>`.


.. figure:: /_static/images/en-us_image_0000001676072105.png
   :alt: **Figure 6** Viewing exception statistics about SQL calls

   **Figure 6** Viewing exception statistics about SQL calls

.. _apm_07_0010__en-us_topic_0000001217564316_table16208113154714:

.. table:: **Table 3** Exception parameters

   ========== ============= ==========================================
   Metric Set Metric        Description
   ========== ============= ==========================================
   Exception  causeType     Exception class
   \          exceptionType Exception type
   \          Count         Number of exceptions
   \          SQL           SQL statement that encounters an exception
   \          Error Stack   Exception stack information
   \          Message       Error message
   ========== ============= ==========================================

**Overview**

On the **Overview** tab page, view the call trend of the selected instance. For details about the metrics, see :ref:`Table 4 <apm_07_0010__en-us_topic_0000001217564316_table37611034174720>`.


.. figure:: /_static/images/en-us_image_0000001676192573.png
   :alt: **Figure 7** Overview

   **Figure 7** Overview

.. _apm_07_0010__en-us_topic_0000001217564316_table37611034174720:

.. table:: **Table 4** Overview parameters

   ========== ============ ======================================
   Metric Set Metric       Description
   ========== ============ ======================================
   Overview   Calls        Total number of calls
   \          Rows Read    Total number of read rows
   \          Avg RT (ms)  Average response time (ms)
   \          Errors       Total number of errors
   \          Rows Updated Number of rows updated in the database
   ========== ============ ======================================

**Info**

On the **Info** tab page, view the driver version information. Click the text in blue to view more details.


.. figure:: /_static/images/en-us_image_0000001676273437.png
   :alt: **Figure 8** Info

   **Figure 8** Info

Viewing Druid Connection Pool Monitoring Data
---------------------------------------------

The Druid connection pool monitoring system collects data sources, connection details, additional configurations, and exception information. You can click |image5| in the upper right corner of the list to customize the columns you want to view. For details about the metrics, see :ref:`Table 5 <apm_07_0010__en-us_topic_0000001217564316_table1274416195551>`.

.. _apm_07_0010__en-us_topic_0000001217564316_table1274416195551:

.. table:: **Table 5** Druid connection pool parameters

   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   | Metric Set               | Metric                               | Description                                                                                                  |
   +==========================+======================================+==============================================================================================================+
   | Data source              | Connection Address                   | Connection address                                                                                           |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Driver                               | Driver name                                                                                                  |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Initialized Connections              | Number of initialized connections                                                                            |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Min Idle Connections in Pool         | Minimum of idle connections in a pool                                                                        |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Max Idle Connections in Pool         | Maximum number of idle connections in a pool                                                                 |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Max Connections in Pool              | Maximum number of connections in a pool                                                                      |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Idle Connections                     | Number of idle connections                                                                                   |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Max Idle Connections                 | Maximum number of idle connections                                                                           |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Active Connections                   | Number of active connections                                                                                 |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Max Active Connections               | Maximum number of active connections                                                                         |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Waiting Threads                      | Number of waiting threads                                                                                    |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Max Waiting Threads                  | Maximum number of waiting threads                                                                            |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Upper Limit for Waiting Threads      | Upper limit for waiting threads                                                                              |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Total Connections                    | Total number of connections                                                                                  |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   | Connection details       | Connection Address                   | Connection address                                                                                           |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Calls                                | Number of calls                                                                                              |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Total RT (ms)                        | Total response time (ms)                                                                                     |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Avg RT (ms)                          | Average response time (ms)                                                                                   |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Errors                               | Number of errors                                                                                             |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Max Concurrency                      | Maximum number of concurrent connections                                                                     |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Max RT (ms)                          | Maximum response time                                                                                        |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | 0 ms-10 ms                           | Number of requests with 0 ms-10 ms response time                                                             |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | 10 ms-100 ms                         | Number of requests with 10 ms-100 ms response time                                                           |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | 100 ms-500 ms                        | Number of requests with 100 ms-500 ms response time                                                          |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | 500 ms-1s                            | Number of requests with 500 ms-1s response time                                                              |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | 1s-10s                               | Number of requests with 1s-10s response time                                                                 |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | 10s-n                                | Number of requests with response time longer than 10s                                                        |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   | Additional configuration | Connection Address                   | Connection address                                                                                           |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Max Wait (ms)                        | Maximum waiting time                                                                                         |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Test on Borrow                       | Whether to verify the validity of a connection before obtaining it from the connection pool                  |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Test on Return                       | Whether to verify the validity of a connection when it is returned                                           |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Test While Idle                      | Whether to verify the validity of an idle connection when an application applies for it from the pool        |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Remove Abandoned                     | Whether to automatically reclaim timeout connections                                                         |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Remove Abandoned TimeoutMillis (ms)  | If a connection in the pool is not returned within the specified duration, the connection will be reclaimed. |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Remove Abandoned Count               | Number of timeout connection reclaims                                                                        |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Min Evictable Idle TimeMillis (ms)   | Minimum idle time of a connection in the pool                                                                |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Time Between EvictionRunsMillis (ms) | Interval for checking the validity of idle connections                                                       |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   | Exception                | causeType                            | Exception class                                                                                              |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Exception Type                       | Exception type                                                                                               |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Count                                | Number of times the exception has occurred                                                                   |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Error Message                        | Message returned when the exception has occurred                                                             |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   |                          | Error Stack                          | Exception stack information                                                                                  |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+
   | Version                  | Driver Version                       | Driver version                                                                                               |
   +--------------------------+--------------------------------------+--------------------------------------------------------------------------------------------------------------+

-  Click a number in blue (such as those in the **Calls** or **Avg RT (ms)** column) to view more details.
-  Click the text in blue (such as those in the **Driver** or **Driver Version** column) to view more details.


.. figure:: /_static/images/en-us_image_0000001675954833.png
   :alt: **Figure 9** Viewing Druid connection pool monitoring data

   **Figure 9** Viewing Druid connection pool monitoring data

.. |image1| image:: /_static/images/en-us_image_0000001569846696.png
.. |image2| image:: /_static/images/en-us_image_0000001277862689.png
.. |image3| image:: /_static/images/en-us_image_0000001650953141.png
.. |image4| image:: /_static/images/en-us_image_0000001278062153.png
.. |image5| image:: /_static/images/en-us_image_0000001471158206.png
