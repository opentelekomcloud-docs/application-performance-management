:original_name: apm_07_1118.html

.. _apm_07_1118:

Data Masking
============

You can set policies to mask the data reported using APM APIs.

Constraints
-----------

APM will collect and store masked data. Do not upload privacy or sensitive data to APM. If you need to upload such data, encrypt them.

Viewing a Data Masking Configuration
------------------------------------

#. Log in to the management console.
#. Click |image1| on the left and choose **Application** > **Application Performance Management**.
#. In the tree on the left, choose **System Management** > **Data Masking** and select your target node. The configuration information is displayed.
#. In the search box, enter a configuration name keyword and click the search icon or press **Enter**.

Adding a Data Masking Configuration
-----------------------------------

#. In the navigation pane, choose **System Management** > **Data Masking** and select your target node.
#. Click **Add Configuration** and set configuration parameters.

   .. table:: **Table 1** Configuration parameters

      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Parameter                         | Description                                                                                                                                                                                                                                                                                                                     |
      +===================================+=================================================================================================================================================================================================================================================================================================================================+
      | Configuration Name                | Used to identify a data masking configuration. This parameter cannot be empty. Enter up to 30 characters. Only letters, digits, and special characters are allowed.                                                                                                                                                             |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Description                       | Used to describe the data masking configuration. This parameter cannot be empty. Enter up to 1,000 characters. Only letters, digits, and special characters are allowed.                                                                                                                                                        |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
      | Configuration Item                | -  Enter up to 32 characters. Only letters, digits, underscores (_), and hyphens (-) are allowed.                                                                                                                                                                                                                               |
      |                                   | -  The configuration item cannot be empty. By default, an empty configuration item is displayed. If you select **Hash code**, content will be replaced with a globally unique random character string. If you select **Mask**, content will be replaced with a fixed number of asterisks (*). By default, **Mask** is selected. |
      |                                   | -  Click the plus sign (+) to add a configuration item, or click the minus sign (-) to delete one.                                                                                                                                                                                                                              |
      |                                   | -  Each configuration can contain up to 20 configuration items.                                                                                                                                                                                                                                                                 |
      |                                   | -  The **httpMethod**, **remoteAddr**, **exceptionType**, **content-type**, **charset**, **api_address**, **url**, **method**, **requestBody**, **responseBody**, **exceptionMsg**, **cookie**, and **Cookie** fields have special functions in APM traces and do not support masking.                                          |
      |                                   | -  If you use one of these fields as a key, the system will display a message indicating that an invalid name exists.                                                                                                                                                                                                           |
      +-----------------------------------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Click **Yes**.
#. In the navigation pane, choose **Application Monitoring** > **Tracing**.
#. Specify criteria to query traces and click |image2| to view call parameters.
#. On the **View Call Parameter** page, check the value of **transactionNames**. It is displayed as **\*******\***.

Modifying a Data Masking Configuration
--------------------------------------

#. In the navigation pane, choose **System Management** > **Data Masking** and select your target node.
#. Click **Modify** in the **Operation** column to modify the configuration.
#. Click **Yes**.

Deleting a Data Masking Configuration
-------------------------------------

#. In the navigation pane, choose **System Management** > **Data Masking** and select your target node.
#. Click **Delete** in the **Operation** column. In the displayed dialog box, click **Yes** to delete the configuration.
#. Select multiple data masking configurations and click **Batch Delete** above the list. In the displayed dialog box, click **Yes** to delete multiple data masking configurations at a time.

.. |image1| image:: /_static/images/en-us_image_0000002136680226.png
.. |image2| image:: /_static/images/en-us_image_0000002136680230.png
