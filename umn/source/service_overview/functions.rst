:original_name: apm_01_0003.html

.. _apm_01_0003:

Functions
=========

APM manages cloud application performance. It provides application metric monitoring, tracing, application topology, URL tracing, tag management, intelligent alarm reporting, Agent management, configuration management, and system management.

Application Metric Monitoring
-----------------------------

This function enables you to monitor the overall health status of applications. It includes application monitoring details, application monitoring settings, monitoring item views, instances, collection status, and component settings.

-  Application monitoring details: APM Agents collect JVM, GC, service call, exception, external call, database access, and middleware metrics of Java applications to help you monitor their conditions.
-  Application monitoring settings: You can customize collection parameters for some collectors.
-  Monitoring item views: APM supports summary tables, trend graphs, latest data tables, and raw data tables.

Tracing
-------

APM comprehensively monitors calls and displays service execution traces and statuses, helping you quickly locate performance bottlenecks and faults.

-  In the displayed trace list, click the target trace to view its basic information.
-  On the trace details page, you can view the trace's complete information, including the local method stack and remote call relationships.

Application Topology
--------------------

Application topologies include:

-  Single-component topology: topology of a single component under a certain environment. You can also view the call relationships of direct and indirect upstream and downstream components.
-  Global application topology: topology of some or all components under an application.

The topology displays the call relationships between services within a period. The statistics can be collected from the caller or the callee. You can also view the trend. On the topology, you can view the call relationships between services and check whether the calls between services are normal to quickly locate faults. The application relationships, call data (service and instance metrics), and health status are clearly displayed.

URL Tracing
-----------

If you need to find out the call relationships of an important application (for example, calling an e-commerce system's API to create orders), use URL tracing analysis. In APM, URL tracing consumes a large number of resources. Therefore, an entry URL will not be added for tracing by default. However, you can set that if necessary. APM has a limit on the total number of URLs added for tracing. It focuses on tracing the downstream calls for the APIs that are added for tracing. Through URL tracing, you can monitor the call relationships between important APIs and downstream services, and detect problems more precisely.

Tag Management
--------------

You can add tags for different environments and applications for easy management.

Intelligent Alarms
------------------

When an application connected to APM meets a preset alarm condition, an alarm is triggered and reported. In this way, you can quickly learn about service exceptions and rectify faults to prevent loss.

APM supports alarm configuration. You can create multiple alarm policies and bind them to nodes.

With the intelligent alarm function, specified personnel can receive SMS or email alarm notifications.

Agent Management
----------------

You can view the deployment and running statuses of the Agents that are connected to APM, and to stop, start, or delete them.

System Management
-----------------

**System Management**: includes **Collection Center**, **Data Masking**, **Usage Statistics**, **Access Keys**, and **General Configuration**.

-  **Collection Center**: displays collectors in a centralized manner. You can view and manage various collectors, metrics, and collection parameters supported by APM.
-  **Data Masking**: You can set data masking policies. The data reported using APM APIs will be masked based on the policies you set.
-  **Usage Statistics**: After Agents are connected, you can check **Agent Statistics** on the **Usage Statistics** page.

-  **Access Keys**: Access Key ID (AK) and Secret Access Key (SK) are your long-term identity credentials. JavaAgents report data with an AK. An AK is used together with an SK to sign requests cryptographically, ensuring that the requests are secret, complete, and correct.
-  **General Configuration**: You can determine whether to collect data through bytecode instrumentation, and specify the slow request threshold and maximum number of rows to collect .
