:original_name: apm_07_0009.html

.. _apm_07_0009:

Call
====

This function monitors the calls of external services by the current application. It covers CSEConsumer, ApacheHttpClient, ApacheHttpAsyncClient, DubboConsumer, and HttpClient monitoring.

This section focuses on HttpClient monitoring.

Going to the Call Page
----------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click |image2| next to the target environment.

#. Click the **Call** tab. By default, the HttpClient monitoring information of all instances is displayed.


   .. figure:: /_static/images/en-us_image_0000001627264696.png
      :alt: **Figure 1** External call data

      **Figure 1** External call data

#. On the displayed **Call** tab page, select a target instance and monitoring item to view the monitoring data in different metric sets.


   .. figure:: /_static/images/en-us_image_0000001676184865.png
      :alt: **Figure 2** Selecting an instance and monitoring item

      **Figure 2** Selecting an instance and monitoring item

#. Select a time range. Default: **Last 20 minutes**.

   Options: **Last 20 minutes**, **Last hour**, **Last 3 hours**, **Last 6 hours**, **Last day**, **Today**, **Yesterday**, **Last week**, **Last month**, or **Custom**.


   .. figure:: /_static/images/en-us_image_0000001651752769.png
      :alt: **Figure 3** Selecting a time range

      **Figure 3** Selecting a time range

#. Click |image3| in the upper right corner of the list and select the metric data you want to view.

Viewing HttpClient Monitoring Data
----------------------------------

**URL summary**

The HttpClient monitoring system collects the metrics of each URL. For details about the metrics, see :ref:`Table 1 <apm_07_0009__en-us_topic_0000001262004153_table43721153163916>`. Click |image4| in the upper right corner of the list and select the metric data you want to view.


.. figure:: /_static/images/en-us_image_0000001675945469.png
   :alt: **Figure 4** URL summary under HttpClient monitoring

   **Figure 4** URL summary under HttpClient monitoring

.. _apm_07_0009__en-us_topic_0000001262004153_table43721153163916:

.. table:: **Table 1** Parameters of URL summary under HttpClient monitoring

   +-------------+-----------------+------------------------------------------------------------------+
   | Metric Set  | Metric          | Description                                                      |
   +=============+=================+==================================================================+
   | URL summary | url             | Called URL.                                                      |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | method          | HTTP method of the URL.                                          |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | Calls           | Number of times that the URL is called.                          |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | Avg RT (ms)     | Average response time of the called URL.                         |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | Errors          | Number of call errors of the URL.                                |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | Max Concurrency | Maximum concurrency of the URL.                                  |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | Max RT (ms)     | Maximum response time of the called URL.                         |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | 0 ms-10 ms      | Number of requests with 0 ms-10 ms response time.                |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | 10 ms-100 ms    | Number of requests with 10 ms-100 ms response time.              |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | 100 ms-500 ms   | Number of requests with 100 ms-500 ms response time.             |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | 500 ms-1s       | Number of requests with 500 ms-1s response time.                 |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | 1s-10s          | Number of requests with 1s-10s response time.                    |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | 10s-n           | Number of requests with response time longer than 10s.           |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | Error Trace     | ID of the trace that encounters an error in a collection period. |
   +-------------+-----------------+------------------------------------------------------------------+
   |             | Slowest Trace   | ID of the slowest trace in a collection period.                  |
   +-------------+-----------------+------------------------------------------------------------------+

-  Click a number in blue (such as those in the **Calls** or **Avg RT (ms)** column) to view more details.
-  Click the text in blue (such as those in the **Slowest Trace** or **Error Trace** column) to view more details.

**Cluster summary**

APM can summarize external call metrics by cluster. For details about the metrics, see :ref:`Table 2 <apm_07_0009__en-us_topic_0000001262004153_table191674445211>`.


.. figure:: /_static/images/en-us_image_0000001627426716.png
   :alt: **Figure 5** Cluster summary under HttpClient monitoring

   **Figure 5** Cluster summary under HttpClient monitoring

.. _apm_07_0009__en-us_topic_0000001262004153_table191674445211:

.. table:: **Table 2** Parameters of cluster summary under HttpClient monitoring

   +-----------------+---------------+--------------------------------------------------------+
   | Metric Set      | Metric        | Description                                            |
   +=================+===============+========================================================+
   | Cluster summary | envId         | Cluster ID of the called party.                        |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | hostUri       | Host URL                                               |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | Calls         | Number of times that the cluster URL is called.        |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | Avg RT (ms)   | Average response time for calling the cluster URL.     |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | Errors        | Number of call errors of the URL.                      |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | Max RT (ms)   | Maximum response time for calling the cluster URL.     |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | 0 ms-10 ms    | Number of requests with 0 ms-10 ms response time.      |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | 10 ms-100 ms  | Number of requests with 10 ms-100 ms response time.    |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | 100 ms-500 ms | Number of requests with 100 ms-500 ms response time.   |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | 500 ms-1s     | Number of requests with 500 ms-1s response time.       |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | 1s-10s        | Number of requests with 1s-10s response time.          |
   +-----------------+---------------+--------------------------------------------------------+
   |                 | 10s-n         | Number of requests with response time longer than 10s. |
   +-----------------+---------------+--------------------------------------------------------+

Click a number in blue (such as those in the **Calls** or **Avg RT (ms)** column) to view more details.

**Status code summary**

APM can summarize external call metrics by status code. For details about the metrics, see :ref:`Table 3 <apm_07_0009__en-us_topic_0000001262004153_table962120572>`.


.. figure:: /_static/images/en-us_image_0000001675947013.png
   :alt: **Figure 6** Status code summary under HttpClient monitoring

   **Figure 6** Status code summary under HttpClient monitoring

.. _apm_07_0009__en-us_topic_0000001262004153_table962120572:

.. table:: **Table 3** Parameters of status code summary under HttpClient monitoring

   +---------------------+------------+------------------------------------------------+
   | Metric Set          | Metric     | Description                                    |
   +=====================+============+================================================+
   | Status code summary | code       | Status code.                                   |
   +---------------------+------------+------------------------------------------------+
   |                     | Count      | Number of times that the status code occurred. |
   +---------------------+------------+------------------------------------------------+
   |                     | Latest URL | URL that returns the status code.              |
   +---------------------+------------+------------------------------------------------+

-  Click a status code in the **code** column. The tracing page is displayed, showing the invocation condition of the status code of the selected instance in the environment in last 20 minutes (default).
-  Click a number in the **Count** column to view the trend of the status code in a specified period.
-  Click the latest URL to view the invocation details of the corresponding status code.

**Exception**

On the **Exception** tab page, view the exception statistics about HttpClient calls. For details about the metrics, see :ref:`Table 4 <apm_07_0009__en-us_topic_0000001262004153_table847310368015>`.


.. figure:: /_static/images/en-us_image_0000001627268020.png
   :alt: **Figure 7** HttpClient monitoring exceptions

   **Figure 7** HttpClient monitoring exceptions

.. _apm_07_0009__en-us_topic_0000001262004153_table847310368015:

.. table:: **Table 4** Parameters of HttpClient monitoring exceptions

   ========== ============= =============================================
   Metric Set Metric        Description
   ========== ============= =============================================
   Exception  causeType     Exception class.
   \          exceptionType Exception type.
   \          Count         Number of times the exception occurred.
   \          Error Message Message returned when the exception occurred.
   \          Error Stack   Exception stack information.
   ========== ============= =============================================

-  Click a number in blue in the **Count** column to view the trend of the thread in a specified period.
-  Click the text in blue in the **Error Message** column to view message details.
-  Click **Detail** in the **Error Stack** column to view exception details.
-  Click **History** in the **Error Stack** column to view the historical error stack list.

**Overview**

On the **Overview** tab page, view the metrics of the selected instance. For details about the metrics, see :ref:`Table 5 <apm_07_0009__en-us_topic_0000001262004153_table714417141030>`.


.. figure:: /_static/images/en-us_image_0000001676267965.png
   :alt: **Figure 8** Overview under HttpClient monitoring

   **Figure 8** Overview under HttpClient monitoring

.. _apm_07_0009__en-us_topic_0000001262004153_table714417141030:

.. table:: **Table 5** Overview parameters of HttpClient monitoring

   ========== =========== =======================
   Metric Set Metric      Description
   ========== =========== =======================
   Overview   Calls       Total number of calls.
   \          Avg RT (ms) Average response time
   \          Errors      Total number of errors.
   ========== =========== =======================

.. |image1| image:: /_static/images/en-us_image_0000001620923917.png
.. |image2| image:: /_static/images/en-us_image_0000001946011769.png
.. |image3| image:: /_static/images/en-us_image_0000001914389876.png
.. |image4| image:: /_static/images/en-us_image_0000001914229960.png
