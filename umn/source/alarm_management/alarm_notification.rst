:original_name: apm_07_0026.html

.. _apm_07_0026:

Alarm Notification
==================

Alarms can be sent to specified terminals by SMS message, email, or function. In this way, you can obtain component exceptions in a timely manner and quickly rectify faults to avoid service loss. Ensure that you have the SMN permission. For details, see *Simple Message Notification (SMN) User Guide*.

If you do not create any notification object, no alarm notifications will be received. To view alarms, log in to the APM console and choose **Alarm Center** > **Alarm List** in the navigation pane.

Creating a Notification Object
------------------------------

#. Log in to the management console.
#. Click |image1| on the left and choose **Application** > **Application Performance Management**.
#. In the navigation pane, choose **Application Monitoring** > **Metrics**.
#. In the tree on the left, click an application. The metric details page of the application is displayed.

5. Click the **Notifications** tab.

6. Click **Add**.


   .. figure:: /_static/images/en-us_image_0000001677135825.png
      :alt: **Figure 1** Creating a notification object

      **Figure 1** Creating a notification object

7. On the displayed page, specify **Region** and **Topic**, and determine whether to enable default notification. If it is enabled, alarm notifications will be sent based on the topic and region you specify.

   -  If no topic is available, create one.
   -  If default notification is enabled, alarms will be sent to the specified region when you create an alarm policy.

8. Click **Yes**.

.. |image1| image:: /_static/images/en-us_image_0000001542186458.png
