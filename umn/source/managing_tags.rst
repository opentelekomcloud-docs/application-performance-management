:original_name: apm_07_1017.html

.. _apm_07_1017:

Managing Tags
=============

You can add tags for different environments and applications for easy management.

Tag management covers tags and global tags.

A tag is used to set a collector corresponding to the monitoring item under one or more environments of an application.

A global tag is used to set a collector corresponding to the monitoring item under all environments of an application.

.. note::

   Priority: Global tag collector configuration > Tag collector configuration > Collector configuration of a monitoring item under an environment

Adding a Tag
------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the navigation tree, select a target application.

#. Click the **Tags** tab.

#. Click **Add Tag**.


   .. figure:: /_static/images/en-us_image_0000001676779877.png
      :alt: **Figure 1** Adding a tag

      **Figure 1** Adding a tag

#. On the page that is displayed, set **Tag** and **Description**, and select the environment to be associated.

   .. table:: **Table 1** Tag parameters

      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                             |
      +===================================+=========================================================================================================================+
      | Tag                               | Enter 1 to 128 characters. Only digits, letters, underscores (_), hyphens (-), brackets, and periods (.) are allowed.   |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------+
      | Description                       | Enter up to 1000 characters. Only digits, letters, underscores (_), hyphens (-), brackets, and periods (.) are allowed. |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------+
      | Bind Environment                  | -  Search by component, environment, or application name is supported.                                                  |
      |                                   | -  You can select one or more environments.                                                                             |
      +-----------------------------------+-------------------------------------------------------------------------------------------------------------------------+

#. Click **Yes**.

Modifying a Tag
---------------

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the navigation tree, select a target application.

#. Click the **Tags** tab.

#. Locate the row that contains the tag to be modified and click **Collector Configuration** in the **Operation** column. In the dialog box that is displayed, select your desired collector from the drop-down list and click **Yes**.

   Locate the row that contains the tag to be modified and click **Change Environment** in the **Operation** column. In the dialog box that is displayed, select your desired environment and click **Yes**.

   Locate the row that contains the tag to be modified and click **Modify Tag** in the **Operation** column. In the dialog box that is displayed, modify the tag and description.


   .. figure:: /_static/images/en-us_image_0000001676862057.png
      :alt: **Figure 2** Modifying a tag

      **Figure 2** Modifying a tag

Deleting a Tag
--------------

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the navigation tree, select a target application.

#. Click the **Tags** tab.

#. Locate the row that contains the target tag and click **Delete** in the **Operation** column. Alternatively, select the tags to delete and click **Delete** above the tag list.


   .. figure:: /_static/images/en-us_image_0000001676864041.png
      :alt: **Figure 3** Deleting a tag

      **Figure 3** Deleting a tag

#. In the dialog box that is displayed, click **Yes**.

Global Tag Collector Configuration
----------------------------------

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the navigation tree, select a target application.

#. Click the **Tags** tab.

#. Click **Global tag collector configuration**.


   .. figure:: /_static/images/en-us_image_0000001628065096.png
      :alt: **Figure 4** Global tag collector configuration

      **Figure 4** Global tag collector configuration

#. Select a collector from the drop-down list and click **Yes**. For details about how to configure monitoring items, see :ref:`Application Monitoring Configuration <apm_07_0011>`.

.. |image1| image:: /_static/images/en-us_image_0000001592577449.png
