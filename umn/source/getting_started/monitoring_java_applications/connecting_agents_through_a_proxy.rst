:original_name: apm_02_0004.html

.. _apm_02_0004:

Connecting Agents Through a Proxy
=================================

The network between your host and APM must be normal. If the network is disconnected, use a proxy.

You can run the **curl -kv** command to check the network.

Constraints
-----------

-  Agents later than 2.4.1 support access through a proxy.
-  Java supports enhanced Agents.

.. _apm_02_0004__en-us_topic_0000001241035473_section8132103817447:

Modifying the apm.config File
-----------------------------

Add **apm.proxy** to the configuration file, as shown in the following figure. Format: "apm.proxy=ip:port".

.. _apm_02_0004__en-us_topic_0000001241035473_section1458519142214:

Obtaining the AK/SK Required for Connecting JavaAgents
------------------------------------------------------

-  Log in to the APM console.

-  Click |image1| on the left and choose **Application** > **Application Performance Management**.

-  Choose **System Management** > **Access Keys** in the navigation pane to obtain the required AK/SK.


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

4. Modify the **apm.config** file in the JavaAgent package. For details, see :ref:`Modifying the apm.config File <apm_02_0004__en-us_topic_0000001241035473_section8132103817447>`. For details about how to configure **master.address**, see :ref:`Access Addresses <apm_02_0008__en-us_topic_0000001266768045_table201446686>`. Enter the AK/SK obtained in :ref:`Obtaining the AK/SK Required for Connecting JavaAgents <apm_02_0004__en-us_topic_0000001241035473_section1458519142214>` to the configuration file, as shown in the following figure.


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

.. |image1| image:: /_static/images/en-us_image_0000002409351828.png
