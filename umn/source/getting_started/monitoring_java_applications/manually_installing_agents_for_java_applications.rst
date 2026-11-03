:original_name: apm_02_0004.html

.. _apm_02_0004:

Manually Installing Agents for Java Applications
================================================

Prerequisites
-------------

-  The network between your host and APM is normal.

   You can run the **Telnet** command to check the network.

   If the network is not connected, use a proxy instead.

-  The AK/SK required for accessing JavaAgents have been obtained. To obtain them, log in to the APM console and choose **System Management** > **Access Keys** in the navigation pane.


   .. figure:: /_static/images/en-us_image_0000001627629722.png
      :alt: **Figure 1** Obtaining an AK/SK

      **Figure 1** Obtaining an AK/SK

Procedure
---------

#. Use a remote login tool, such as PuTTY, to log in to the Linux host where the Agent is to be installed and run related commands as the **root** user.

#. Download JavaAgent to any directory on the host to be connected to APM. For details, see :ref:`JavaAgent Download Addresses <apm_02_0007__en-us_topic_0000001222407900_table145112051071>`.

   Example command:

   **curl -O https://xxx/apm-javaagent-x.x.x.tar**

3. Run the **tar** command to decompress the JavaAgent package.

   Example command:

   **tar -xvf apm-javaagent-x.x.x.tar**

4. Modify the **apm.config** file in the JavaAgent package. For details about how to configure **master.address**, see :ref:`Access Addresses <apm_02_0008__en-us_topic_0000001266768045_table201446686>`. Enter the AK/SK to the configuration file, as shown in the following figure.


   .. figure:: /_static/images/en-us_image_0000001196275562.png
      :alt: **Figure 2** Adding the AK/SK

      **Figure 2** Adding the AK/SK

5. Modify the startup script of the Java process.

   Add the path of the **apm-javaagent.jar** package and the component name of the Java process to the end of the Java command in the service startup script.

   Example of adding **-javaagent** parameters:

   java **-javaagent:/xxx/apm-javaagent/apm-javaagent.jar=appName={appName}**

   If your enterprise has a large number of services, you can add more complex configurations. For example:

   java **-javaagent:/xxx/apm-javaagent/apm-javaagent.jar=appName=myApp,env=myEnv,envTag=myTag,business=myBusiness,subBusiness=mySub**

   -  The preceding parameters are built-in CMDB information of APM. For details, see :ref:`CMDB Management <apm_07_0050>`.

   -  Due to historical reasons, the metadata of APM startup parameters conflicts with some CMDB concepts. The following shows the details.

      Generally, the startup parameter is set to **-javaagent:D:\\javaagent-package\\apm-javaagent\\apm-javaagent.jar=appName=xxx,env=yyy,business=zzz,subBusiness=sss,envTag=xxx**. **appName** indicates a component, **business** indicates an application, **subBusiness** indicates a sub-application, and **envTag** indicates an environment tag.

      If **business** is not set on the web page, the system reports an error when the JavaAgent is started. If other parameters (**subBusiness**, **appName**, **env**, and **envTag**) are not set, the system automatically creates them when the JavaAgent is started.

      Component names are unique under an application.

6. Redeploy the application.
