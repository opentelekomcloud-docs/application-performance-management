:original_name: apm_07_1018.html

.. _apm_07_1018:

Data Masking
============

You can set policies to mask the data reported using APM.

.. important::

   APM will collect and store masked data. Do not upload privacy or sensitive data to APM. If you need to upload such data, encrypt it.

Querying a Data Masking Configuration
-------------------------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation tree on the left, choose **Configuration Management** > **Data Masking** and select your target node. The configuration information is displayed.


   .. figure:: /_static/images/en-us_image_0000001908141568.png
      :alt: **Figure 1** Viewing a data masking configuration

      **Figure 1** Viewing a data masking configuration

#. In the search box, enter a configuration name keyword and click the search icon or press **Enter**.


   .. figure:: /_static/images/en-us_image_0000001908141536.png
      :alt: **Figure 2** Searching for a configuration

      **Figure 2** Searching for a configuration

Adding a Data Masking Configuration
-----------------------------------

#. In the navigation tree on the left, choose **Configuration Management** > **Data Masking** and select your target node.


   .. figure:: /_static/images/en-us_image_0000001908301536.png
      :alt: **Figure 3** Configuring data masking

      **Figure 3** Configuring data masking

#. Click **Add** and set configuration parameters.


   .. figure:: /_static/images/en-us_image_0000001908301484.png
      :alt: **Figure 4** Adding a configuration

      **Figure 4** Adding a configuration

   .. table:: **Table 1** Configuration parameters

      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                                                                                 |
      +===================================+=============================================================================================================================================================================================================================================================================================================================+
      | Configuration Name                | Used to identify a data masking configuration. This parameter cannot be empty. Enter up to 30 characters. Only letters, digits, and special characters are allowed.                                                                                                                                                         |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Configuration Description         | Used to describe the data masking configuration. This parameter cannot be empty. Enter up to 1000 characters. Only letters, digits, and special characters are allowed.                                                                                                                                                     |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Configuration Items               | -  Enter up to 32 characters. Only letters, digits, underscores (_), and hyphens (-) are allowed.                                                                                                                                                                                                                           |
      |                                   | -  The configuration item cannot be empty. By default, an empty configuration item is displayed. If you select **Token**, content will be replaced with a globally unique random character string. If you select **Mask**, content will be replaced with a fixed number of asterisks (*). By default, **Mask** is selected. |
      |                                   | -  Click the plus sign (+) to add a configuration item, or click the minus sign (-) to delete one.                                                                                                                                                                                                                          |
      |                                   | -  Each configuration can contain up to 20 configuration items.                                                                                                                                                                                                                                                             |
      |                                   | -  The **httpMethod**, **remoteAddr**, **exceptionType**, **content-type**, **charset**, **api_address**, **url**, **method**, **requestBody**, **responseBody**, **exceptionMsg**, **cookie**, and **Cookie** fields have special functions in APM traces and do not support masking.                                      |
      |                                   | -  If you use one of these fields as a key, the system will display a message indicating that an invalid name exists.                                                                                                                                                                                                       |
      +-----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **Yes**.

Modifying a Data Masking Configuration
--------------------------------------

#. In the navigation tree on the left, choose **Configuration Management** > **Data Masking** and select your target node.

#. Click **Modify** in the **Operation** column to modify the configuration.


   .. figure:: /_static/images/en-us_image_0000001908301500.png
      :alt: **Figure 5** Modifying the data masking configuration

      **Figure 5** Modifying the data masking configuration

#. Click **Yes**.

Deleting Data Masking Configurations
------------------------------------

#. In the navigation tree on the left, choose **Configuration Management** > **Data Masking** and select your target node.

#. Click **Delete** in the **Operation** column. In the displayed dialog box, click **Yes** to delete the configuration.


   .. figure:: /_static/images/en-us_image_0000001908141492.png
      :alt: **Figure 6** Deleting the data masking configuration

      **Figure 6** Deleting the data masking configuration

#. Select multiple data masking configurations and click **Batch Delete** above the list. In the displayed dialog box, click **Yes** to delete multiple data masking configurations at a time.


   .. figure:: /_static/images/en-us_image_0000001943060789.png
      :alt: **Figure 7** Deleting configurations in batches

      **Figure 7** Deleting configurations in batches

.. |image1| image:: /_static/images/en-us_image_0000001943060829.png
