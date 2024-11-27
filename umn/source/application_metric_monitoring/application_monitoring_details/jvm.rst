:original_name: apm_07_0007.html

.. _apm_07_0007:

JVM
===

This function monitors JVMInfo, JVMMonitor, GC, thread, and JavaMethod.

Going to the JVM Page
---------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click |image2| next to the target environment.

#. Click the **JVM** tab. By default, the JVMMonitor information of all instances is displayed.


   .. figure:: /_static/images/en-us_image_0000001676256889.png
      :alt: **Figure 1** Going to the JVM page

      **Figure 1** Going to the JVM page

#. On the displayed **JVM** tab page, select a target instance and monitoring item to view the monitoring data in different metric sets.


   .. figure:: /_static/images/en-us_image_0000001676257513.png
      :alt: **Figure 2** Selecting an instance and monitoring item

      **Figure 2** Selecting an instance and monitoring item

#. Select a time range. Default: **Last 20 minutes**.

   Options: **Last 20 minutes**, **Last hour**, **Last 3 hours**, **Last 6 hours**, **Last day**, **Today**, **Yesterday**, **Last week**, **Last month**, or **Custom**.


   .. figure:: /_static/images/en-us_image_0000001651751305.png
      :alt: **Figure 3** Selecting a time range

      **Figure 3** Selecting a time range

Viewing JVM Information
-----------------------

On the **JVM** tab page, view the JVMInfo metrics of the corresponding instance. For details about the metrics, see :ref:`Table 1 <apm_07_0007__en-us_topic_0000001217724300_table157251648155319>`.


.. figure:: /_static/images/en-us_image_0000001627418708.png
   :alt: **Figure 4** Viewing JVM information

   **Figure 4** Viewing JVM information

.. _apm_07_0007__en-us_topic_0000001217724300_table157251648155319:

.. table:: **Table 1** JVMInfo metrics

   ========== ========================== ===========================
   Metric Set Metric                     Description
   ========== ========================== ===========================
   JVMInfo    JavaAgent Version          Java Agent version.
   \          Started                    JVM startup time.
   \          Startup Parameter          JVM startup parameter.
   \          Java Class Library Path    Java class library path.
   \          Java Version               Java version.
   \          Java Specification Version Java specification version.
   \          OS                         OS name.
   \          OS Version                 OS version.
   \          arch                       CPU architecture.
   \          Processors                 Number of processors.
   \          SDK Version                SDK version.
   ========== ========================== ===========================

Viewing JVM Monitoring Data
---------------------------

APM monitors JVM metrics. For details about the metrics, see :ref:`Table 2 <apm_07_0007__en-us_topic_0000001217724300_table1215310405>`. JVM monitoring metrics are displayed in graphs, so that you can view and analyze JVM monitoring data more easily.


.. figure:: /_static/images/en-us_image_0000001627739144.png
   :alt: **Figure 5** Viewing JVM monitoring data

   **Figure 5** Viewing JVM monitoring data

.. _apm_07_0007__en-us_topic_0000001217724300_table1215310405:

.. table:: **Table 2** JVM monitoring metrics

   +---------------+-----------------------+--------------------------------------------+
   | Metric Set    | Metric                | Description                                |
   +===============+=======================+============================================+
   | Thread        | Current Threads       | Number of current threads.                 |
   +---------------+-----------------------+--------------------------------------------+
   |               | Deadlock Threads      | Number of deadlock threads.                |
   +---------------+-----------------------+--------------------------------------------+
   |               | Daemon Threads        | Number of daemon threads.                  |
   +---------------+-----------------------+--------------------------------------------+
   |               | Started Threads       | Number of started threads.                 |
   +---------------+-----------------------+--------------------------------------------+
   |               | Peak Threads          | Peak number of threads.                    |
   +---------------+-----------------------+--------------------------------------------+
   | Thread Status | Waiting Threads       | Number of waiting threads.                 |
   +---------------+-----------------------+--------------------------------------------+
   |               | Terminated Threads    | Number of threads in the terminated state. |
   +---------------+-----------------------+--------------------------------------------+
   |               | Runnable Threads      | Number of runnable threads.                |
   +---------------+-----------------------+--------------------------------------------+
   |               | Blocked Threads       | Number of blocked threads.                 |
   +---------------+-----------------------+--------------------------------------------+
   |               | New Threads           | Number of new threads.                     |
   +---------------+-----------------------+--------------------------------------------+
   |               | Timed Waiting Threads | Number of threads that timed out.          |
   +---------------+-----------------------+--------------------------------------------+
   | Memory        | Used Non-Heap Memory  | Size of the used non-heap memory.          |
   +---------------+-----------------------+--------------------------------------------+
   |               | Used Heap Memory      | Size of the used heap memory.              |
   +---------------+-----------------------+--------------------------------------------+
   |               | Used Direct Memory    | Size of the used direct memory.            |
   +---------------+-----------------------+--------------------------------------------+
   | Class loading | Current Classes       | Number of current classes.                 |
   +---------------+-----------------------+--------------------------------------------+
   |               | Total Loaded Classes  | Total number of loaded classes.            |
   +---------------+-----------------------+--------------------------------------------+
   |               | Unloaded Classes      | Number of unloaded classes.                |
   +---------------+-----------------------+--------------------------------------------+
   | Memory pool   | committed(M)          | Size of available memory.                  |
   +---------------+-----------------------+--------------------------------------------+
   |               | init(M)               | Size of the initialized memory.            |
   +---------------+-----------------------+--------------------------------------------+
   |               | max(M)                | Size of the maximum memory.                |
   +---------------+-----------------------+--------------------------------------------+
   |               | name                  | Memory pool name.                          |
   +---------------+-----------------------+--------------------------------------------+
   |               | used(M)               | Size of the used memory.                   |
   +---------------+-----------------------+--------------------------------------------+
   | CPU           | CPU Usage             | CPU usage of the Java process.             |
   +---------------+-----------------------+--------------------------------------------+

Viewing GC Information
----------------------

APM monitors GC metrics. For details about the metrics, see :ref:`Table 2 <apm_07_0007__en-us_topic_0000001217724300_table1215310405>`.


.. figure:: /_static/images/en-us_image_0000001676260081.png
   :alt: **Figure 6** Viewing GC information

   **Figure 6** Viewing GC information

.. table:: **Table 3** GC metrics

   +---------------+------------------------+--------------------------------------------------+
   | Metric Set    | Metric                 | Description                                      |
   +===============+========================+==================================================+
   | GC statistics | Full GC (times)        | Number of full GC times in a collection period.  |
   +---------------+------------------------+--------------------------------------------------+
   |               | Full GC Duration (ms)  | Full GC duration in a collection period.         |
   +---------------+------------------------+--------------------------------------------------+
   |               | Young GC (times)       | Number of young GC times in a collection period. |
   +---------------+------------------------+--------------------------------------------------+
   |               | Young GC Duration (ms) | Young GC duration in a collection period.        |
   +---------------+------------------------+--------------------------------------------------+
   | GC Details    | GC Type                | GC type, which can be **major** or **minor**.    |
   +---------------+------------------------+--------------------------------------------------+
   |               | GC Cause               | GC cause.                                        |
   +---------------+------------------------+--------------------------------------------------+
   |               | Count                  | Number of times that GC has occurred.            |
   +---------------+------------------------+--------------------------------------------------+
   |               | Total GC Duration (ms) | GC duration.                                     |
   +---------------+------------------------+--------------------------------------------------+
   |               | Max GC Duration (ms)   | Time consumed by the slowest GC.                 |
   +---------------+------------------------+--------------------------------------------------+
   |               | GC Recycler            | GC recycler name.                                |
   +---------------+------------------------+--------------------------------------------------+
   |               | Slowest GC Details     | Details about the slowest GC.                    |
   +---------------+------------------------+--------------------------------------------------+

-  Click the digits in blue (such as those in the **Count**, **Total GC Duration (ms)**, or **Max GC Duration (ms)** column) to view the corresponding GC trend graph in a certain period (default: 20 minutes).
-  On the GC details area, you can view the GC type, GC cause, count, total GC duration (ms), maximum GC duration (ms), GC recycler, and slowest GC details (details and history).

Viewing Threads
---------------

You can view the thread details of the corresponding instance on APM. For details, see :ref:`Table 4 <apm_07_0007__en-us_topic_0000001217724300_table3735183811019>`.


.. figure:: /_static/images/en-us_image_0000001627740904.png
   :alt: **Figure 7** Viewing threads

   **Figure 7** Viewing threads

.. _apm_07_0007__en-us_topic_0000001217724300_table3735183811019:

.. table:: **Table 4** Thread metrics

   ============== ============= ==================
   Metric Set     Metric        Description
   ============== ============= ==================
   Thread details Thread Name   Thread name.
   \              Threads       Number of threads.
   \              CPU Time (ms) Thread CPU time.
   \              Memory (MB)   Memory (MB).
   \              Thread Stack  Thread stack.
   ============== ============= ==================

-  Click a number in the **Threads** column to view the trend of the thread in a specified period.
-  Click **Detail** in the **Thread Stack** column to view the thread details.
-  Click **History** in the **Thread Stack** column to view the historical thread stack list.

Viewing Java Methods
--------------------

#. By default, APM does not monitor Java methods. To monitor them, :ref:`configure the JavaMethod monitoring item <apm_07_0016>` first.
#. After the configuration is complete, the system monitors the methods and classes of JavaMethod.
#. On the **JVM** page, select a target instance and **JavaMethod** to view details. For details, see :ref:`Table 5 <apm_07_0007__en-us_topic_0000001217724300_table16330184212241>`.


.. figure:: /_static/images/en-us_image_0000001627262204.png
   :alt: **Figure 8** Viewing Java methods

   **Figure 8** Viewing Java methods

.. _apm_07_0007__en-us_topic_0000001217724300_table16330184212241:

.. table:: **Table 5** JavaMethod metrics

   +------------+-----------------+--------------------------------------------------------+
   | Metric Set | Metric          | Description                                            |
   +============+=================+========================================================+
   | JavaMethod | Class           | Class of a Java method.                                |
   +------------+-----------------+--------------------------------------------------------+
   |            | Method          | Method.                                                |
   +------------+-----------------+--------------------------------------------------------+
   |            | Calls           | Number of times that the method is called.             |
   +------------+-----------------+--------------------------------------------------------+
   |            | Avg RT (ms)     | Average response time.                                 |
   +------------+-----------------+--------------------------------------------------------+
   |            | Errors          | Number of times that the method fails to be called.    |
   +------------+-----------------+--------------------------------------------------------+
   |            | Max Concurrency | Maximum concurrency of the method.                     |
   +------------+-----------------+--------------------------------------------------------+
   |            | Max RT (ms)     | Maximum response time of the method.                   |
   +------------+-----------------+--------------------------------------------------------+
   |            | 0 ms-10 ms      | Number of requests with 0 ms-10 ms response time.      |
   +------------+-----------------+--------------------------------------------------------+
   |            | 10 ms-100 ms    | Number of requests with 10 ms-100 ms response time.    |
   +------------+-----------------+--------------------------------------------------------+
   |            | 100 ms-500 ms   | Number of requests with 100 ms-500 ms response time.   |
   +------------+-----------------+--------------------------------------------------------+
   |            | 500 ms-1s       | Number of requests with 500 ms-1s response time.       |
   +------------+-----------------+--------------------------------------------------------+
   |            | 1s-10s          | Number of requests with 1s-10s response time.          |
   +------------+-----------------+--------------------------------------------------------+
   |            | 10s-n           | Number of requests with response time longer than 10s. |
   +------------+-----------------+--------------------------------------------------------+

-  Click a number (such as those in the **Calls** or **Errors** column) to view the trend of the thread in a specified period.

.. |image1| image:: /_static/images/en-us_image_0000001570285326.png
.. |image2| image:: /_static/images/en-us_image_0000001913972706.png
