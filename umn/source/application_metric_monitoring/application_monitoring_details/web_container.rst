:original_name: apm_07_0061.html

.. _apm_07_0061:

Web Container
=============

This function monitors web containers, including Tomcat. This section focuses on Tomcat monitoring.

Going to the Web Container Page
-------------------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click |image2| next to the target environment.

#. Click the **Web Container** tab. By default, the Tomcat monitoring information of all instances is displayed. For details about the metrics, see :ref:`Table 1 <apm_07_0061__en-us_topic_0000001568155621_table737216573912>`.


   .. figure:: /_static/images/en-us_image_0000001675956117.png
      :alt: **Figure 1** Going to the web container page

      **Figure 1** Going to the web container page

   .. _apm_07_0061__en-us_topic_0000001568155621_table737216573912:

   .. table:: **Table 1** Tomcat monitoring parameters

      +------------------------+---------------------+----------------------------------------------------------------------+
      | Metric Set             | Metric              | Description                                                          |
      +========================+=====================+======================================================================+
      | Tomcat port monitoring | name                | Port name.                                                           |
      +------------------------+---------------------+----------------------------------------------------------------------+
      |                        | Current Threads     | Number of current threads on the port.                               |
      +------------------------+---------------------+----------------------------------------------------------------------+
      |                        | Busy Threads        | Number of busy threads on the port at the time of collection.        |
      +------------------------+---------------------+----------------------------------------------------------------------+
      |                        | Peak Busy Threads   | Maximum number of busy threads on the port in a collection period.   |
      +------------------------+---------------------+----------------------------------------------------------------------+
      |                        | Max Threads         | Maximum number of threads on the port.                               |
      +------------------------+---------------------+----------------------------------------------------------------------+
      |                        | Max Connections     | Maximum number of connections on the port.                           |
      +------------------------+---------------------+----------------------------------------------------------------------+
      |                        | Current Connections | Number of current connections of the port at the time of collection. |
      +------------------------+---------------------+----------------------------------------------------------------------+
      |                        | Peak Connections    | Maximum number of connections on the port in a collection period.    |
      +------------------------+---------------------+----------------------------------------------------------------------+
      | Version                | Version             | Tomcat version.                                                      |
      +------------------------+---------------------+----------------------------------------------------------------------+

   -  Click a number in blue (such as those in the **Current Threads**, **Busy Threads**, or **Peak Busy Threads** column) to view the trend graph of the target web container in the specified period.
   -  Click a version in the **Version** column to view details.

#. On the displayed **Web Container** tab page, select a target instance and monitoring item to view the monitoring data in different metric sets.


   .. figure:: /_static/images/en-us_image_0000001627439044.png
      :alt: **Figure 2** Selecting an instance and monitoring item

      **Figure 2** Selecting an instance and monitoring item

#. Select a time range. Default: **Last 20 minutes**.

   Options: **Last 20 minutes**, **Last hour**, **Last 3 hours**, **Last 6 hours**, **Last day**, **Today**, **Yesterday**, **Last week**, **Last month**, or **Custom**.


   .. figure:: /_static/images/en-us_image_0000001602670490.png
      :alt: **Figure 3** Selecting a time range

      **Figure 3** Selecting a time range

#. Click |image3| in the upper right corner of the list and select the metric data you want to view.

.. |image1| image:: /_static/images/en-us_image_0000001620725989.png
.. |image2| image:: /_static/images/en-us_image_0000001946011753.png
.. |image3| image:: /_static/images/en-us_image_0000001946109001.png
