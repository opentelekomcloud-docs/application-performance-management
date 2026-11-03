:original_name: apm_02_0005.html

.. _apm_02_0005:

Installing Agents for the Java Applications Deployed in CCE Containers
======================================================================

.. _apm_02_0005__en-us_topic_0000001195795614_section8132103817447:

Prerequisites
-------------

-  You are advised to install self-developed Agents for the Java applications deployed in CCE containers.

-  The network between your host and APM is normal.

   You can run the **Telnet** command to check the network.

-  For details, see `Regions and Endpoints <https://docs.otc.t-systems.com/regions-and-endpoints/index.html>`__.

-  The AK/SK required for accessing JavaAgents have been obtained. To obtain them, log in to the APM console and choose **System Management** > **Access Keys** in the navigation pane.


   .. figure:: /_static/images/en-us_image_0000002188473004.png
      :alt: **Figure 1** Obtaining an AK/SK

      **Figure 1** Obtaining an AK/SK

Usage Instruction
-----------------

APM only supports Java applications deployed on CCE. :ref:`Table 1 <apm_02_0005__en-us_topic_0000001195795614_table182631618114215>` describes the parameters.

.. _apm_02_0005__en-us_topic_0000001195795614_table182631618114215:

.. table:: **Table 1** Parameters for configuring performance management

   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Name                              | Description                                                                                                                                           |
   +===================================+=======================================================================================================================================================+
   | Probe                             | Select a target probe. Options: **Disable**/**APM probe**.                                                                                            |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Probe Version                     | Version of the probe. You are advised to select a probe version based on the CPU architecture of the node where the workload is located.              |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Probe Upgrade Policy              | Policy for the probe upgrade. The default value is **Auto upgrade upon restart**.                                                                     |
   |                                   |                                                                                                                                                       |
   |                                   | -  **Automatic upgrade upon restart**: The system downloads the probe image each time the pod is restarted.                                           |
   |                                   | -  **Manual upgrade**: If a local image is available, it will be used. If no local image is available, the system downloads the probe image.          |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+
   | APM Environment                   | Enter an APM environment name. This parameter is optional.                                                                                            |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+
   | APM App                           | Select an existing APM application.                                                                                                                   |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Sub-app                           | Enter an APM sub-application. This parameter is optional.                                                                                             |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Access Key                        | The system automatically obtains the APM key. For details, see :ref:`Prerequisites <apm_02_0005__en-us_topic_0000001195795614_section8132103817447>`. |
   +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------+

Procedure
---------

#. Log in to the CCE console. In the navigation pane, choose **Workloads** > **Deployments** or **StatefulSets**, and click **Create Deployment** or **Create StatefulSet**.

#. In the **APM Settings** area on the **Configure Advanced Settings** page, select **Java probe**. The APM service will be enabled and a probe will be installed on the node.

   Probes provide traces, topologies, SQL analysis, and stack tracing for Java workloads. A small number of resources will be consumed when you run probes.

#. Set probe-related parameters.

   -  **Monitoring Group**: Enter a monitoring group name, for example, **testapp**. Select a group from the drop-down list if there are any.
   -  **Probe Version**: Select a probe version.
   -  **Probe Upgrade Policy**: By default, **Automatic upgrade upon restart** is selected.

      -  **Automatic upgrade upon restart**: The system downloads the probe image each time the pod is restarted.
      -  **Manual upgrade**: If a local image is available, it will be used. If no local image is available, the system downloads the probe image.

#. After the application is started, wait for about 3 minutes. Then, the application data is displayed on the APM console. You can log in to the APM console and optimize the application performance through topology and tracing.
