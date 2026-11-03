:original_name: apm_07_0004.html

.. _apm_07_0004:

Introduction
============

APM Agents periodically collect performance metric data to measure the overall health status of applications. They can collect the metric data of JVM, GC, service calls, exceptions, external calls, database access, and middleware, helping you comprehensively monitor application running.

APM has strict definitions on metric data collection. Each type of data to be collected corresponds to a collector. For example, for JVM data of Java applications, a JVM collector is provided. A collector collects data of multiple metric sets. For details about collectors and metric sets, see :ref:`Collection Center <apm_07_0031>`.

After collectors are deployed in the environment, monitoring items are generated. During data collection, the monitoring items determine data structures and collection behaviors.

-  Collection period: A monitoring item has the same period attribute as a data collector. The default data collection period is 1 minute and cannot be changed.
-  Monitoring item status: A monitoring item is enabled by default. You can disable it so that an Agent does not intercept or report the metric data. For details, see :ref:`Enabling or Disabling a Monitoring Item <apm_07_0012__en-us_topic_0000001262919611_section5159143418218>`.
-  Collection status: Each collection instance or monitoring item has a collection status. If a collection error occurs, you can view it on the **Collection Status** tab page. A common error is that there are too many primary keys. As a result, data aggregation on the client is abnormal.

Monitoring Item Types
---------------------

Agents automatically discover collection plug-ins and instantiate collectors to form monitoring items. Monitoring items are instantiated in an environment.

There are many types of collectors, which are hard to distinguish. The system backend groups collectors for easy data query.

The **Metrics** page displays only the involved monitoring item metrics of connected applications.

Based on collector functions, monitoring items can be classified into:

-  **Topology**: displays the call relationships between services within a period. The statistics can be collected from the caller or the callee. You can also check the trend.
-  **URL**: monitors the external services that call the current application.
-  **JVM**: monitors basic system performance metrics.
-  **Exception**: monitors application exceptions.
-  **Call**: monitors the external services called by the current application.
-  **SQL**: monitors database access.
-  **Web Container**: monitors web containers such as Tomcat. Generally, the total number of threads, number of busy threads, and number of connections are collected to measure the overall system capacity.

Monitoring Item Configuration
-----------------------------

Collectors corresponding to monitoring items define collection parameters. You can modify collection parameters on the page as required. These parameters will be delivered to Agents with heartbeat parameters to change collection behaviors. By default, Redis instruction content is not collected for security purposes. If necessary, modify collection parameters to collect specific instruction data. Collection parameters can also be defined on environment tags. Collectors automatically inherit collection parameter attributes of corresponding environment tags. In this way, configuration is automated.

Monitoring Item Views
---------------------

On the metric monitoring details page, a monitoring item corresponds to one or more tab views, and each view corresponds to a metric set. APM provides summary tables, trend graphs, latest data tables, and original tables. For details, see :ref:`Monitoring Item Views <apm_07_0017>`.
