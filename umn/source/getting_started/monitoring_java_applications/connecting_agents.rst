:original_name: apm_02_0003.html

.. _apm_02_0003:

Connecting Agents
=================

Prerequisites
-------------

-  The network between your host and APM is normal. You can run the **curl -kv** command to check the network.
-  Java supports enhanced Agents.

Procedure
---------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **Application Monitoring** > **Applications**.

#. On the displayed page, click **Connect Application**.


   .. figure:: /_static/images/en-us_image_0000001675786929.png
      :alt: **Figure 1** Connecting an application

      **Figure 1** Connecting an application

#. Select a region and application. Click **Create Application**. In the dialog box that is displayed, create an application by referring to :ref:`Creating an Application <apm_07_0151>`.


   .. figure:: /_static/images/en-us_image_0000001627467410.png
      :alt: **Figure 2** Basic information

      **Figure 2** Basic information

#. Select **Enhanced Agent** for **Access Mode**.

#. Select **Java** for **Backend Language**.


   .. figure:: /_static/images/en-us_image_0000001881092662.png
      :alt: **Figure 3** Access mode

      **Figure 3** Access mode

#. Use a remote login tool, such as PuTTY, to log in to the Linux host where the Agent is to be installed and run related commands as the user with the root or service permissions.

#. Select an access mode based on the application type and access data by following the instructions.

   -  Enhanced Agent

      -  VM Access

         a. Choose **System Management** > **Access Keys** and obtain the AK and SK required by the Java Agent.

         b. Use a remote login tool, such as PuTTY, to log in to the Linux host where the Agent is to be installed and run related commands as the user with the **root** or **service** permissions. Use the account who starts the application to run the installation command.

         c. Download and install JavaAgent:

            .. code-block::

               curl -k https://obs-eu-de-apm2-gamma.obs.eu-de.otctest.t-systems.com/apm_agent_install2.sh -o apm_agent_install.sh && bash apm_agent_install.sh -ak {APM_AK} -sk {APM_SK} -masteraddress https://100.125.7.25:41333 -obsaddress https://obs-eu-de-apm2-gamma.obs.eu-de.otctest.t-systems.com -version latest; history -cw; history -r

            .. table:: **Table 1** VM access parameters

               +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
               | Parameter             | Description                                                                                                                                                                                                                         | Mandatory             |
               +=======================+=====================================================================================================================================================================================================================================+=======================+
               | APM_AK                | AK and SK for installing JavaAgent. To obtain **APM_AK** and **APM_SK**, see :ref:`Access Keys <apm_07_0034>`.                                                                                                                      | Yes                   |
               |                       |                                                                                                                                                                                                                                     |                       |
               | APM_SK                | When you copy the command to install JavaAgent, delete **{}** when setting **APM_AK** and **APM_SK**.                                                                                                                               |                       |
               |                       |                                                                                                                                                                                                                                     |                       |
               |                       | Example:                                                                                                                                                                                                                            |                       |
               |                       |                                                                                                                                                                                                                                     |                       |
               |                       | .. code-block::                                                                                                                                                                                                                     |                       |
               |                       |                                                                                                                                                                                                                                     |                       |
               |                       |    curl -k https://javaagent.***/apm_agent_install2.sh -o apm_agent_install.sh && bash apm_agent_install.sh -ak * -sk * -masteraddress https://**** -obsaddress https://javaagent.***.com -version latest; history -cw; history -r  |                       |
               +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
               | masteraddress         | Access address. For details, see :ref:`Access Addresses <apm_02_0008>`.                                                                                                                                                             | Yes                   |
               +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
               | version               | Agent version. The latest Agent provided by APM supports multiple JDK environments.                                                                                                                                                 | Yes                   |
               +-----------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

         d. Add the startup command and restart the application. It takes about 1 minute to install the Agent. After the installation is complete, add JVM parameters to the startup script of your application and then restart it. Startup command format:

            .. code-block::

               java -javaagent:Agent installation path/apm-javaagent/apm-javaagent.jar=appName=Component name,env=Environment name,envTag=Environment tag,business=Application alias,subBusiness=Sub-application name -jar User application.jar

            Example of a startup command:

            .. code-block::

               java -javaagent:/root/my-dir/apm-javaagent/apm-javaagent.jar=appName=my-service,env=dev -jar test-2.0.0-SNAPSHOT.jar

            .. table:: **Table 2** Startup command parameters

               +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------+
               | Parameter               | Description                                                                                                                                                                                                                                                                                                  | Mandatory |
               +=========================+==============================================================================================================================================================================================================================================================================================================+===========+
               | Agent Installation Path | Path for installing the Agent.                                                                                                                                                                                                                                                                               | Yes       |
               +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------+
               | Component Name          | Component name, which must start with a letter. Each component name must be unique under an application. A component can contain multiple environments. If there are duplicate names, use **instanceName** to distinguish them.                                                                              | Yes       |
               +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------+
               | Environment Name        | Name of an environment where an application is deployed. A program can be deployed in different environments (such as the test or live network environment). Each environment is deployed in one region and has a unique region attribute. If this parameter is blank, the default environment will be used. | No        |
               +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------+
               | Environment Labels      | Environment tag for filtering environments. Different environments may have the same tag. This parameter can be left blank.                                                                                                                                                                                  | No        |
               +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------+
               | App Name                | Name of an application (a global concept). Create an application before specifying this parameter. If this parameter is left blank, the automatically created application will be used.                                                                                                                      | No        |
               +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------+
               | Sub-application Name    | Sub-application (a global concept). It is a subfolder under the application. If this parameter is left blank, resources will be mounted to the root application. Up to three layers of sub-applications are supported. For example, for **a/b/c**, each represents one layer.                                | No        |
               +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------+
               | User Application        | Name of a user application.                                                                                                                                                                                                                                                                                  | Yes       |
               +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------+

.. |image1| image:: /_static/images/en-us_image_0000001737607793.png
