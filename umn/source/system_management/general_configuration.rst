:original_name: apm_07_0035.html

.. _apm_07_0035:

General Configuration
=====================

On the **General Configuration** page, you can determine whether to collect data through bytecode instrumentation, and specify the slow request threshold and maximum number of rows to collect.

#. Log in to the management console.

#. Click |image1| on the left and choose **Management & Deployment** > **Application Performance Management**.

#. In the navigation pane, choose **System Management** > **General Configuration**.


   .. figure:: /_static/images/en-us_image_0000001628908238.png
      :alt: **Figure 1** Modifying general configuration

      **Figure 1** Modifying general configuration

   -  Stop Collecting Data Through Bytecode Instrumentation

      Enable or disable this function as required. Data such as JVM metrics will always be collected using MBeans. The default value is **No**.

      .. note::

         When the **Stop Collecting Data Through Bytecode Instrumentation** option is enabled, data will no longer be collected through bytecode instrumentation. Data such as JVM, GC, and Tomcat thread metrics can still be collected using MBeans.

   -  Slow Request Threshold

      If this threshold is reached, more samples will be collected during intelligent sampling. The default value is **800**.

   -  Max. Collected Data Rows

      If this value is reached, data will not be collected to prevent excessive memory usage. The default value is **499**.

.. |image1| image:: /_static/images/en-us_image_0000001542557752.png
