:original_name: apm_07_0019.html

.. _apm_07_0019:

Application Topology
====================

On the tracing page, you can view the topology of a single call, as well as the overall topology between different services based on collected metric data. There are two types of application topologies:

-  Single-component topology: topology of a single component under an environment. You can also view the call relationships of direct and indirect upstream and downstream components.
-  Global application topology: topology of some or all components under an application.

Each line in the topology indicates the call relationship between services within a period. The statistics can be collected from the calling or called party. You can click a line to view the call trend on the right. The topology can also display the call relationships between middleware. On the topology, you can view the call relationships between services and check whether the calls between services are normal to quickly locate faults.

Viewing the Topology of a Component
-----------------------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click |image2| next to the target environment.

#. Click the **Topology** tab to view the call and dependency relationships of the component.

   Click a line between components. The detailed data is displayed on the right.

   Enable **Display only calls between components** to shield the calls of external components, or click **Show All** to display the calls between all components except the central node.

#. Right-click a component and then click **Viewing a Call Chain** or **Viewing Indicators**.

   -  Viewing a call chain

      Click **Viewing a Call Chain** to go to the trace page of the component. For details, see :ref:`Tracing <apm_07_0018>`.

   -  Viewing indicators

      Click **Viewing Indicators** to go to the URL page of the component. For details, see :ref:`URL <apm_07_0006>`.

Viewing the Global Topology
---------------------------

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click an application. The application details page is displayed.

#. Click the **Global Topology** tab to view the call and dependency relationships of all components under the application.

   -  Click a line between components. The detailed data is displayed on the right.
   -  Enable **Display only calls between components** to shield the calls of external components.
   -  Use tags to filter calls.


   .. figure:: /_static/images/en-us_image_0000001676682349.png
      :alt: **Figure 1** Viewing the global topology

      **Figure 1** Viewing the global topology

.. |image1| image:: /_static/images/en-us_image_0000001541828576.png
.. |image2| image:: /_static/images/en-us_image_0000001914132538.png
