:original_name: apm_07_0020.html

.. _apm_07_0020:

URL Tracing
===========

You can view the topology of a single call, as well as the overall topology between different services. In some scenarios, the call relationships of an important business need to be traced. This process is called URL tracing. For example, to trace the API for creating online shopping orders. In APM, URL tracing consumes a large number of resources. Therefore, an entry URL will not be added for tracing by default. However, you can set that if necessary. APM has a limit on the total number of URLs added for tracing. It focuses on tracing the downstream calls for the APIs that are added for tracing. Through URL tracing, you can monitor the call relationships between important APIs and downstream services, and then detect problems more precisely.

.. _apm_07_0020__en-us_topic_0000001254639833_section178672317113:

Configuring URL Tracing
-----------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Management & Deployment** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click the environment that needs URL tracing. The environment details page is displayed. By default, the **URL** tab page is displayed.

#. Move the mouse pointer to the target URL, click |image2|, and add it for URL tracing.


   .. figure:: /_static/images/en-us_image_0000001628010336.png
      :alt: **Figure 1** Configuring URL tracing

      **Figure 1** Configuring URL tracing

Checking the URL Tracing View
-----------------------------

-  On the **URL** tab page:

   For the URL added for tracing, click |image3| next to it to view its topology.


   .. figure:: /_static/images/en-us_image_0000001676692165.png
      :alt: **Figure 2** Viewing URL tracing details

      **Figure 2** Viewing URL tracing details

-  On the **URL Tracing Views** tab page:

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click an application. The application details page is displayed.

#. Click the **URL Tracing Views** tab to check all URL tracing views of the application.

#. Filter transaction views by region and environment.

#. Click **View** in the **Operation** column of the row that contains the URL you want to view.


   .. figure:: /_static/images/en-us_image_0000001628013376.png
      :alt: **Figure 3** Checking the URL tracing view

      **Figure 3** Checking the URL tracing view

Viewing the URL Tracing Configuration
-------------------------------------

The URL which has been added for tracing will be displayed in the URL tracing configuration list.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click an application. The application details page is displayed.

#. Click the **URL Tracing Configuration** tab to check all URL tracing configurations of the application.


   .. figure:: /_static/images/en-us_image_0000001627855218.png
      :alt: **Figure 4** Viewing the URL tracing configuration list

      **Figure 4** Viewing the URL tracing configuration list

#. To delete a URL tracing configuration, click **Delete** in the **Operation** column.


   .. figure:: /_static/images/en-us_image_0000001628335774.png
      :alt: **Figure 5** Deleting a URL tracing configuration

      **Figure 5** Deleting a URL tracing configuration

Viewing Transactions
--------------------

Transaction URLs are displayed in a list. By default, the system displays the invocation of all entries.

#. In the navigation pane, choose **Application Monitoring** > **Metrics**.

#. In the tree on the left, click an application. The application details page is displayed.

#. Click the **Transactions** tab to view all transactions of the application.


   .. figure:: /_static/images/en-us_image_0000001628339878.png
      :alt: **Figure 6** Viewing transactions

      **Figure 6** Viewing transactions

#. Click **View the call chain** in the **Operation** column of the target transaction. For operations related to call chains, see :ref:`Tracing <apm_07_0018>`.


   .. figure:: /_static/images/en-us_image_0000001676580969.png
      :alt: **Figure 7** Viewing the call chain

      **Figure 7** Viewing the call chain

.. |image1| image:: /_static/images/en-us_image_0000001570166220.png
.. |image2| image:: /_static/images/en-us_image_0000001277858573.png
.. |image3| image:: /_static/images/en-us_image_0000001233739060.png
