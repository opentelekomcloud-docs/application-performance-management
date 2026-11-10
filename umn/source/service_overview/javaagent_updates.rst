:original_name: apm_01_0093.html

.. _apm_01_0093:

JavaAgent Updates
=================

Constraints
-----------

-  To download Agents, see :ref:`JavaAgent Download Addresses <apm_02_0007>`.
-  Agent download rules:

   -  2.5.x and later versions: JDK versions will no longer be distinguished in the download addresses of Agents.

      For example, the download address for Agent 2.5.5 is **https://apm2-javaagent**\ ``***``\ **/apm2_javaagent/apm-javaagent-2.5.5.tar**.

   -  Versions earlier than 2.5.x: If a version ends with **-jdk17**, add **-jdk17** to the end of the Agent download path.

      For example, if the download address for Agent 2.4.8 is **https://apm2-javaagent**\ ``***``\ **/apm2_javaagent/apm-javaagent-2.4.8.tar**, that address for Agent 2.4.8-jdk17 will be **https://apm2-javaagent**\ ``***``\ **/apm2_javaagent/apm-javaagent-2.4.8-jdk17.tar**.

.. table:: **Table 1** JavaAgent updates

   +-----------------------------------+----------------------------------------------------------------------------------------------------------+
   | Version                           | Description                                                                                              |
   +===================================+==========================================================================================================+
   | 2.5.7                             | #. Supported the ApusicAS9.0 framework.                                                                  |
   |                                   | #. Fixed the issue that trace IDs were not transferred when Tomcat and Reactor Netty coexisted.          |
   |                                   | #. Optimized the metric and trace reporting performance.                                                 |
   |                                   | #. Optimized Java method configuration logic and enabled the configuration to take effect automatically. |
   |                                   | #. Combined JavaAgent versions.                                                                          |
   |                                   | #. Optimized concurrency increase logic.                                                                 |
   +-----------------------------------+----------------------------------------------------------------------------------------------------------+
   | 2.4.8-jdk17                       | #. Supported Redisson 3.17.x.                                                                            |
   |                                   | #. Supported TP on the URL page.                                                                         |
   +-----------------------------------+----------------------------------------------------------------------------------------------------------+
   | 2.4.8                             | #. Supported Redisson 3.17.x.                                                                            |
   |                                   | #. Supported top percentile (TP) on the URL page.                                                        |
   |                                   |                                                                                                          |
   |                                   |    .. note::                                                                                             |
   |                                   |                                                                                                          |
   |                                   |       a. The 2.4.8 version only supports JDK 8.                                                          |
   +-----------------------------------+----------------------------------------------------------------------------------------------------------+
   | 2.3.15                            | #. Supported Dubbo 2.8.x.                                                                                |
   |                                   | #. Supported JDK HTTP subclasses.                                                                        |
   +-----------------------------------+----------------------------------------------------------------------------------------------------------+

.. table:: **Table 2** Latest JavaAgent versions on CCE

   +-----------------------------------+-----------------------------------------------------------+
   | Version                           | Actual Version                                            |
   +===================================+===========================================================+
   | latest                            | #. 2.4.8-jdk17; compatible with x86 and Arm architectures |
   +-----------------------------------+-----------------------------------------------------------+
