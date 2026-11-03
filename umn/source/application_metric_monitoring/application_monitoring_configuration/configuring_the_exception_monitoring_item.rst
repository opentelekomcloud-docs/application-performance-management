:original_name: apm_07_0055.html

.. _apm_07_0055:

Configuring the Exception Monitoring Item
=========================================

Constraints
-----------

To record thread names in logs, you need to add **%thread** to the **logback.xml** file.

|image1|

On the **Modify Exception Monitoring Configuration** page, set the following parameters:

-  **Collection Interval**: The default value is **60s** and cannot be changed.
-  **Determine Trace Exception upon Log Error Detection**: The default value is **Yes**. If **Use default value** is selected, the value of the inherited tag is preferentially used.
-  **Associating Service Logs with TraceId**: The default value is **No**. If **Use default value** is selected, the value of the inherited tag is preferentially used.

.. |image1| image:: /_static/images/en-us_image_0000002195699309.png
