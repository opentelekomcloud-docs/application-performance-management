:original_name: apm_01_0004.html

.. _apm_01_0004:

Application Scenarios
=====================

APM is widely used. The following lists some typical scenarios.

Diagnosis of Application Exceptions
-----------------------------------

**Pain Points**

In the distributed microservice architecture, enterprises can develop diverse applications efficiently, but face great challenges in traditional O&M and diagnosis. An e-commerce application may face the following problems:

-  Difficult fault locating

   After receiving the feedback from customers, customer service personnel submit problems to technical personnel for troubleshooting. In the distributed microservice architecture, a request usually undergoes multiple services/nodes before a result is returned. If a fault occurs, O&M personnel need to repeatedly view logs on multiple hosts to locate the fault. Even for simple problems, troubleshooting requires cooperation from multiple teams.

-  Difficult architecture sort-out

   When service logic becomes complex, it is difficult to find out the downstream services (databases, HTTP APIs, and caches) that an application depends on, and external services that depend on the application from the code perspective. It is also difficult to sort out the service logic, manage the architecture, and plan capacities. For example, enterprises are hard to determine the number of hosts required in their activities.

**Service Implementation**

APM can diagnose exceptions in large distributed applications. When an application breaks down or a request fails, you can locate faults in minutes through topologies and drill-downs.

-  Visible topology: Abnormal application instances can be automatically discovered on the topology.
-  Tracing: You can locate root causes in code through drill-downs after identifying abnormal applications.
-  SQL analysis: APM displays graphs of key metrics (such as number of SQL statement calls, latency, and number of errors), and supports analysis of database performance problems caused by abnormal SQL statements.

User Experience Management
--------------------------

**Pain Points**

In the Internet era where user experience is of crucial importance, you cannot obtain user access information even if backend services run stably. It is much more difficult to locate frontend problems that occur occasionally. After a system goes online, if users cannot access the system due to errors and APM fails to obtain the information in time, lots of users will choose to leave. If users report page problems, how can APM reproduce the problems immediately? How can error details be obtained for fast troubleshooting?

**Service Implementation**

APM analyzes the complete process (user request > server > database > server > user request) of application transactions in real time, enabling you to monitor comprehensive user experience in real time. For transactions with poor user experience, locate problems through topologies and tracing.

-  Application KPI analysis: KPIs such as throughput, latency, and call success rate are displayed, so that you can monitor user experience easily.
-  Full-link performance tracing: Web services, caches, and databases are traced, so that you can detect performance bottlenecks quickly.

Intelligent Diagnosis
---------------------

**Pain Points**

Massive services bring abundant but unassociated application O&M data, including hundreds of monitoring metrics, KPI data, and tracing data. How can metric and alarm data be associated for analysis from the application, component, or URL tracing perspective? How can possible causes be provided for exceptions based on the historical data and O&M experience library?

**Service Implementation**

APM supports automatic detection of faults using machine learning algorithms, and intelligent diagnosis. When an exception is found during URL tracing, APM learns historical metric data based on intelligent algorithms, associates exception metrics for multi-dimensional analysis, extracts characteristics of context data (such as resources, parameters, and call structures) for both normal and abnormal services, and locate root causes through cluster analysis.
