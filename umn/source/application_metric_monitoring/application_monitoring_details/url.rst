:original_name: apm_07_0006.html

.. _apm_07_0006:

URL
===

This function monitors the calls of the current application by external services. It includes URL, Dubbo server, CSE server, CSEProvider cluster, and FunctionGraph monitoring. This type of monitoring item demonstrates the actual external status of the entire service. For example, if the average response time of a URL is long, it means that external users take a long time to query the corresponding data.

This section focuses on URL monitoring.

Going to the URL Page
---------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click |image2| next to the target environment. On the **URL** tab page that is displayed, check URL monitoring information of all instances.


   .. figure:: /_static/images/en-us_image_0000001676225985.png
      :alt: **Figure 1** Going to the URL page

      **Figure 1** Going to the URL page

#. On the displayed **URL** tab page, select a target instance and monitoring item to view the monitoring data in different metric sets.


   .. figure:: /_static/images/en-us_image_0000001676226289.png
      :alt: **Figure 2** Selecting an instance and monitoring item

      **Figure 2** Selecting an instance and monitoring item

#. Select a time range. Default: **Last 20 minutes**.

   Options: **Last 20 minutes**, **Last hour**, **Last 3 hours**, **Last 6 hours**, **Last day**, **Today**, **Yesterday**, **Last week**, **Last month**, or **Custom**.


   .. figure:: /_static/images/en-us_image_0000001651751305.png
      :alt: **Figure 3** Selecting a time range

      **Figure 3** Selecting a time range

#. Click |image3| in the upper right corner of the list and select the metric data you want to view.

Viewing URL Monitoring Data
---------------------------

**URL summary**

For common URL calls, the system collects the metrics of each URL. For details about the metrics, see :ref:`Table 1 <apm_07_0006__en-us_topic_0000001262244099_table17761201314410>`.


.. figure:: /_static/images/en-us_image_0000001675906817.png
   :alt: **Figure 4** URL summary under URL monitoring

   **Figure 4** URL summary under URL monitoring

.. _apm_07_0006__en-us_topic_0000001262244099_table17761201314410:

.. table:: **Table 1** Parameters of the URL summary

   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Metric Set  | Metric          | Description                                                                                                                                                             |
   +=============+=================+=========================================================================================================================================================================+
   | URL summary | url             | URL.                                                                                                                                                                    |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | method          | Request HTTP method.                                                                                                                                                    |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | Calls           | Number of times that the URL is called.                                                                                                                                 |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | Avg RT (ms)     | Average response time of the URL in a collection period.                                                                                                                |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | Errors          | Number of call errors of the URL.                                                                                                                                       |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | Max Concurrency | Maximum concurrency of the URL.                                                                                                                                         |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | Max RT (ms)     | Maximum response time of the URL in a collection period.                                                                                                                |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | Apdex           | Application performance index (Apdex), which indicates users' satisfaction. The value ranges from 0 to 1. The closer the value is to 1, the higher the satisfaction is. |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | 0 ms-10 ms      | Number of requests with 0 ms-10 ms response time.                                                                                                                       |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | 10 ms-100 ms    | Number of requests with 10 ms-100 ms response time.                                                                                                                     |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | 100 ms-500 ms   | Number of requests with 100 ms-500 ms response time.                                                                                                                    |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | 500 ms-1s       | Number of requests with 500 ms-1s response time.                                                                                                                        |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | 1s-10s          | Number of requests with 1s-10s response time.                                                                                                                           |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   |             | 10s-n           | Number of requests with response time longer than 10s.                                                                                                                  |
   +-------------+-----------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

-  URL invocation is the starting point of tracing. When you click a URL, the tracing page is displayed, showing the URL invocation condition in a certain period (default: 20 minutes).
-  You can add a URL for tracing by referring to :ref:`Configuring URL Tracing <apm_07_0020__en-us_topic_0000001254639833_section178672317113>`.
-  Click a number in blue (such as those in the **Calls** or **Avg RT (ms)** column) to view more details.

**Status code summary**

APM supports status code-based summary. The system collects the metrics of each URL. For details about the metrics, see :ref:`Table 2 <apm_07_0006__en-us_topic_0000001262244099_table12423123513019>`.


.. figure:: /_static/images/en-us_image_0000001627227794.png
   :alt: **Figure 5** Status code summary under URL monitoring

   **Figure 5** Status code summary under URL monitoring

.. _apm_07_0006__en-us_topic_0000001262244099_table12423123513019:

.. table:: **Table 2** Parameters of status code summary

   +---------------------+------------+------------------------------------------------------------------+
   | Metric Set          | Metric     | Description                                                      |
   +=====================+============+==================================================================+
   | Status code summary | code       | Status code.                                                     |
   +---------------------+------------+------------------------------------------------------------------+
   |                     | Count      | Number of times that the status code occurred.                   |
   +---------------------+------------+------------------------------------------------------------------+
   |                     | Latest URL | Sample URL which returns the status code in a collection period. |
   +---------------------+------------+------------------------------------------------------------------+

-  Click a status code in the **code** column. The tracing page is displayed, showing the invocation condition of the status code of the selected instance in the environment in last 20 minutes (default).
-  Click a number in the **Count** column to view the trend of the status code in a specified period.
-  Click the latest URL to view the invocation details of the corresponding status code.

**Cluster summary**

APM can summarize metrics by cluster. For details about the metrics, see :ref:`Table 3 <apm_07_0006__en-us_topic_0000001262244099_table184262985614>`.


.. figure:: /_static/images/en-us_image_0000001627388978.png
   :alt: **Figure 6** Cluster summary under URL monitoring

   **Figure 6** Cluster summary under URL monitoring

.. _apm_07_0006__en-us_topic_0000001262244099_table184262985614:

.. table:: **Table 3** Parameters of the cluster summary

   +-----------------+-------------+------------------------------------------------------+
   | Metric Set      | Parameter   | Description                                          |
   +=================+=============+======================================================+
   | Cluster summary | Cluster ID  | Cluster ID of the caller.                            |
   +-----------------+-------------+------------------------------------------------------+
   |                 | Calls       | Number of times the cluster is called.               |
   +-----------------+-------------+------------------------------------------------------+
   |                 | Avg RT (ms) | Average response time in a collection period.        |
   +-----------------+-------------+------------------------------------------------------+
   |                 | Errors      | Number of times that the cluster fails to be called. |
   +-----------------+-------------+------------------------------------------------------+

Click a number in blue (such as those in the **Calls** or **Avg RT (ms)** column) to view more details.

**Overview**

View the metric trend of the selected instance on the **Overview** tab page. For details about the metrics, see :ref:`Table 4 <apm_07_0006__en-us_topic_0000001262244099_table19880607475>`.


.. figure:: /_static/images/en-us_image_0000001676029453.png
   :alt: **Figure 7** Overview under URL monitoring

   **Figure 7** Overview under URL monitoring

.. _apm_07_0006__en-us_topic_0000001262244099_table19880607475:

.. table:: **Table 4** Overview metrics

   ========== ============== =================================
   Metric Set Metric         Description
   ========== ============== =================================
   Overview   Total Requests Total number of URL requests.
   \          Avg RT (ms)    Average response time of the URL.
   \          Errors         Total number of URL errors.
   \          Apdex          Users' satisfaction with the URL.
   ========== ============== =================================

.. |image1| image:: /_static/images/en-us_image_0000001570589062.png
.. |image2| image:: /_static/images/en-us_image_0000001946011785.png
.. |image3| image:: /_static/images/en-us_image_0000001650834309.png
