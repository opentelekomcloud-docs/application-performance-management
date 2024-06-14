:original_name: apm_07_0048.html

.. _apm_07_0048:

Configuring the Druid Monitoring Item
=====================================

On the **Modify Druid Monitoring Configuration** page, set the following parameters:

-  **Collection Interval**: The default value is **60s** and cannot be changed.
-  **TraceReportTimeSpanThreshold(ms)**: threshold for reporting getConnection method traces. If the threshold is not exceeded, such traces will not be reported. The default value is **1**. If you select **Use default value**, the value of the inherited tag is preferentially used.
-  **Get pool info when calling getConnection**: specifies whether to obtain the pool information when calling the **getConnection** method. The default value is **No**. If you select **Use default value**, the value of the inherited tag is preferentially used.
