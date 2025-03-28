:original_name: apm_03_0004.html

.. _apm_03_0004:

Why Does APM Metric Collection Fail?
====================================

#. You can check metric data several minutes after you connect APM Agents.
#. If data collection stops, check the following:

   -  Instance level: Agents are stopped on the **Instance** tab page.
   -  Monitoring item level: Monitoring items are manually disabled on the **Monitoring Item** tab page.
   -  Global level: The **Stop Collecting Data Through Bytecode Instrumentation** option is enabled on the **General Configuration** page of APM.

3. If no data is collected for a long time, check the following:

   -  Java 9 prompts that the **sql.time** class cannot be found.

      Cause analysis: Agents are developed using JDK 1.7. However, after Java 9 modularization, no SQL package is provided by default.

      Occurrence: This problem occurs under certain conditions.

      Workaround: Ensure that the component can proactively import **java.sql** to **module-info.java**.

   -  Java 11 prompts that "Caused by: java.lang.NoClassDefFoundError: sun/misc/Unsafe class cannot be found."

      Cause analysis: Agents are developed using JDK 1.7, but the Java 11 Unsafe class is categorized to a different package.

      Occurrence: This problem occurs inevitably.

      Workaround: Ensure that the application can proactively import **jdk.unsupported** to **module-info.java**.

   -  Java 9 reports an illegal reflective access alarm. (This problem will be solved in versions later than Java 9.)

      Workaround: Set **--illegal-access** to **warn** or delete this option.
