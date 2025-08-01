:original_name: apm_07_0008.html

.. _apm_07_0008:

Exception
=========

This function monitors application exception logs. Take the monitoring of Java exception logs as an example. Once you use the log system to print logs, they will be collected by APM. The exception collection type varies according to the collector type.

Viewing Exception Logs
----------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click |image2| next to the target environment.

#. Click the **Exception** tab. By default, exception logs of all instances are displayed. For details about the metrics, see :ref:`Table 1 <apm_07_0008__en-us_topic_0000001262364087_table121125341047>`.

   .. _apm_07_0008__en-us_topic_0000001262364087_table121125341047:

   .. table:: **Table 1** Exception and log parameters

      +-------------+------------------+------------------------------------------------+
      | Metric Set  | Parameter        | Description                                    |
      +=============+==================+================================================+
      | Exception   | Class            | Exception class                                |
      +-------------+------------------+------------------------------------------------+
      |             | Exception Type   | Exception type                                 |
      +-------------+------------------+------------------------------------------------+
      |             | Log Type         | Exception log type                             |
      +-------------+------------------+------------------------------------------------+
      |             | Total Exceptions | Number of times that an exception has occurred |
      +-------------+------------------+------------------------------------------------+
      |             | Message          | Message returned when the exception occurred   |
      +-------------+------------------+------------------------------------------------+
      |             | Error Stack      | Error stack                                    |
      +-------------+------------------+------------------------------------------------+
      | Log Version | Log Type         | Log type                                       |
      +-------------+------------------+------------------------------------------------+
      |             | Version          | Version                                        |
      +-------------+------------------+------------------------------------------------+

   -  Click a number in pink in the **Total Exceptions** column to view the trend of the total exceptions in a specified period.
   -  Click the pink text in the **Message** column to view the message time and content.
   -  Click **Detail** in the **Error Stack** column to view exception details.
   -  Click **History** in the **Error Stack** column to view the historical error stack list.

   -  Click the pink text in the **Version** column to view details.

#. On the **Exception** tab page, select a target instance and then select **Exception** to view the exception monitoring data.

#. Select a time range. Default: **Last 20 minutes**.

   Options: **Last 20 minutes**, **Last hour**, **Last 3 hours**, **Last 6 hours**, **Last day**, **Today**, **Yesterday**, **Last week**, **Last month**, or **Custom**.

#. Click |image3| in the upper right corner of the list and select the metric data you want to view.

.. |image1| image:: /_static/images/en-us_image_0000001621004377.png
.. |image2| image:: /_static/images/en-us_image_0000001946011777.png
.. |image3| image:: /_static/images/en-us_image_0000001914389884.png
