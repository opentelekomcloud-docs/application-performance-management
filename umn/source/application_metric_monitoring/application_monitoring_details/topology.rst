:original_name: apm_07_0067.html

.. _apm_07_0067:

Topology
========

The topology displays the call relationships between services within a period. The statistics can be collected from the caller or the callee. You can also view the trend. On the topology, you can view the call relationships between services and check whether the calls between services are normal to quickly locate faults. The application relationships, call data (service and instance metrics), and health status are clearly displayed.

Viewing the Topology
--------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click |image2| next to the target environment.

#. Switch to the **Topology** tab page. The call trend of the selected instance is displayed.

#. Click |image3| next to **Display only calls between components**.

   When the button turns pink, only the calls between components are displayed.

#. Click **Show All** to display all call relationships of the selected instance in a specified time range.

#. Click **Reset Layout** to restore to the initial topology.

#. Select the refresh mode and time. Default: **Manual Refresh**. In addition, **Automatic refresh in 1 minute**, **Automatic refresh in 5 minutes**, and **Automatic refresh in 15 minutes** are supported.

#. Select a time range. Default: **Last 20 minutes**.

   Options: **Last 20 minutes**, **Last hour**, **Last 3 hours**, **Last 6 hours**, **Last day**, **Today**, **Yesterday**, **Last week**, **Last month**, or **Custom**.

   -  Click |image4| to refresh the topology.

.. |image1| image:: /_static/images/en-us_image_0000001651367393.png
.. |image2| image:: /_static/images/en-us_image_0000001913838480.png
.. |image3| image:: /_static/images/en-us_image_0000001651699845.png
.. |image4| image:: /_static/images/en-us_image_0000002169235581.png
