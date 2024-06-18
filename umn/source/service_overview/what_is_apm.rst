:original_name: apm_01_0002.html

.. _apm_01_0002:

What Is APM
===========

O&M Challenges
--------------

In the cloud era, applications in the microservice architecture are increasingly diversified, bringing many application exceptions. Application O&M faces the following challenges:

-  Distributed applications have complex relationships. As a result, it is hard to ensure normal application running, and quickly locate faults and performance bottlenecks.
-  Users choose to leave due to poor experience. If O&M personnel cannot detect and trace services with poor experience in real time, or diagnose application exceptions in a timely manner, user experience will be greatly affected.
-  There are a large number of widely distributed applications in the service system. Calls across systems, regions, and applications are frequent. Enterprises urgently need to reduce application management and O&M costs and improve O&M efficiency.

Introduction to APM
-------------------

Application Performance Management (APM) helps O&M personnel quickly identify application performance bottlenecks and locate root causes of faults, ensuring user experience.

You only need to install Agents for applications so that APM can monitor them in an all-round manner. APM can quickly locate error APIs and slow APIs, reproduce calling parameters, and detect system bottlenecks, facilitating online diagnosis. Currently, APM supports Java applications. The following table lists the application monitoring capabilities of APM.

.. note::

   APM is short for Application Performance Management. **apm2** is the registered endpoint address.

.. table:: **Table 1** APM monitoring capabilities

   +----------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Capability                                               | Description                                                                                                                                                                                                                  |
   +==========================================================+==============================================================================================================================================================================================================================+
   | Non-intrusive collection of application performance data | You do not need to modify application code. Instead, you only need to deploy an APM Agent package and modify application startup parameters to monitor applications.                                                         |
   +----------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Application metric monitoring                            | APM automatically monitors application metrics, such as JVM, JavaMethod, URL, Exception, Tomcat, HttpClient, MySQL, Redis, and Kafka.                                                                                        |
   +----------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Application topology                                     | APM automatically generates call relationships between distributed applications based on dynamic analysis and intelligent computing of remote procedure call (RPC) information.                                              |
   +----------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Tracing                                                  | After multiple applications are connected to APM, APM automatically samples requests, and collects the call relationships between services and the health status of intermediate calls for automatic tracing.                |
   +----------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Metric drill-down analysis                               | APM enables you to drill down and analyze metrics such as application response time, number of requests, and error rate, and view metrics by application, component, environment, database, middleware, or other dimensions. |
   +----------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
   | Error or slow URL tracing                                | APM identifies error or slow URLs based on URL tracing, and automatically associates them with corresponding APIs, such as SQL and MQ APIs.                                                                                  |
   +----------------------------------------------------------+------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

#. Access to APM: Applications need to implement AK/SK authentication to connect to APM.
#. O&M data collection: APM can collect data about applications, basic resources, and user experience from Agents in non-intrusive mode.
#. Service implementation: APM supports application metric monitoring, application topology, tracing, and intelligent alarm reporting.
#. Service expansion:

   -  You can quickly diagnose application performance exceptions based on the application topology and tracing of APM, and make judgments based on the application O&M metrics of Application Operations Management (AOM).
   -  Based on the historical metric data learned by using intelligent algorithms, APM associates metrics for analysis from multiple dimensions, extracts the context data of both normal and abnormal services for comparison, and locates root causes through cluster analysis.

Advantages
----------

|image1|

Connects to applications without having to modify code, and collects data in a non-intrusive mode.

-  APM Agents collect service call, service inventory, and call KPI data.

|image2|

Delivers high throughput (hundreds of millions of API calls), ensuring premium experience.

|image3|

Provides open APIs to query O&M data, offers collection standards, and supports independent development.

|image4|

Reports alarms using Artificial Intelligence (AI) threshold detection and machine learning based on historical baseline data, and supports root cause analysis.

.. |image1| image:: /_static/images/en-us_image_0000001278522953.png
.. |image2| image:: /_static/images/en-us_image_0000001278405305.png
.. |image3| image:: /_static/images/en-us_image_0000001234565280.png
.. |image4| image:: /_static/images/en-us_image_0000001278805009.png
