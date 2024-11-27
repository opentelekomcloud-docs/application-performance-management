:original_name: apm_07_0028.html

.. _apm_07_0028:

Operating Agents
================

Agent Management allows you to check the deployment and running statuses of the Agents that are connected to APM, and to stop, start, or delete them.

Checking Agents
---------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Agent Management**.

#. Check the Agent list.

   a. In the upper left corner of the page, select a target region and application.
   b. Set the search criteria and click |image2| in the search box in the upper right corner of the page to filter Agents.


   .. figure:: /_static/images/en-us_image_0000001677017637.png
      :alt: **Figure 1** Viewing Agents

      **Figure 1** Viewing Agents

The following table describes the Agent statuses.

+----------+------------------------------------------------------------------------------+
| Status   | Description                                                                  |
+==========+==============================================================================+
| Enabled  | The Agent is running properly.                                               |
+----------+------------------------------------------------------------------------------+
| Offline  | The Agent is abnormal due to a network error. Check and restore the network. |
+----------+------------------------------------------------------------------------------+
| Disabled | The Agent is manually or globally disabled. Contact technical support.       |
+----------+------------------------------------------------------------------------------+

Batch Operations
----------------

#. In the navigation pane, choose **Application Monitoring** > **Agent Management**.

#. Select target objects and click **Operation**.


   .. figure:: /_static/images/en-us_image_0000001628418878.png
      :alt: **Figure 2** Batch operations

      **Figure 2** Batch operations

#. Select **Disable Agent**, **Enable Agent**, or **Delete Agent**.


   .. figure:: /_static/images/en-us_image_0000001628420042.png
      :alt: **Figure 3** Operating Agents in batches

      **Figure 3** Operating Agents in batches

#. In the dialog box that is displayed, click **Yes** to disable, enable, or delete the Agents for the selected hosts.


   .. figure:: /_static/images/en-us_image_0000001628420554.png
      :alt: **Figure 4** Deleting Agents

      **Figure 4** Deleting Agents

.. |image1| image:: /_static/images/en-us_image_0000001542497618.png
.. |image2| image:: /_static/images/en-us_image_0000001277861629.png
