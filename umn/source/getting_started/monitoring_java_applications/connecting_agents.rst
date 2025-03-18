:original_name: apm_02_0003.html

.. _apm_02_0003:

Connecting Agents
=================

Prerequisites
-------------

The network between your host and APM is normal.

You can run the **Telnet** command to check the network.

.. important::

   Java supports enhanced Agents.

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

#. Select **Java** for **Backend language**.


   .. figure:: /_static/images/en-us_image_0000001881092662.png
      :alt: **Figure 3** Access mode

      **Figure 3** Access mode

#. Select **Enhanced Agent** for **Code Source**.

#. Use a remote login tool, such as PuTTY, to log in to the Linux host where the Agent is to be installed and run related commands as the **root** user.

#. Select an access mode based on the application type and access data by following the instructions.


   .. figure:: /_static/images/en-us_image_0000001627469086.png
      :alt: **Figure 4** Data access

      **Figure 4** Data access

   .. table:: **Table 1** Parameter description

      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Parameter               | Description                                                                                                                                                                                                                                                                                                  | Mandatory             |
      +=========================+==============================================================================================================================================================================================================================================================================================================+=======================+
      | APM_AK                  | AK and SK for installing JavaAgent.                                                                                                                                                                                                                                                                          | Yes                   |
      |                         |                                                                                                                                                                                                                                                                                                              |                       |
      | APM_SK                  | .. caution::                                                                                                                                                                                                                                                                                                 |                       |
      |                         |                                                                                                                                                                                                                                                                                                              |                       |
      |                         |    CAUTION:                                                                                                                                                                                                                                                                                                  |                       |
      |                         |    When you copy the command to install JavaAgent, delete **{}** when setting **APM_AK** and **APM_SK**.                                                                                                                                                                                                     |                       |
      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | Probe Installation Path | Path for installing the Agent.                                                                                                                                                                                                                                                                               | Yes                   |
      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | appName                 | Component name, which must start with a letter. A component can contain multiple environments. The names of components under an application must be unique. If there are duplicate names, use **instanceName** to distinguish them.                                                                          | Yes                   |
      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | env                     | Name of an environment where an application is deployed. A program can be deployed in different environments (such as the test or live network environment). Each environment is deployed in one region and has a unique region attribute. If this parameter is blank, the default environment will be used. | No                    |
      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | envTag                  | Environment tag for filtering environments. Different environments may have the same tag. This parameter can be left blank.                                                                                                                                                                                  | No                    |
      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | business                | Name of an application that already exists (a global concept). If this parameter is left blank, the automatically created application will be used.                                                                                                                                                          | No                    |
      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | subBusiness             | Name of a sub-application (a global concept), which is similar to a folder. If it is left blank, resources will be mounted to the root application. There can be up to three layers of sub-applications. For example, for **a/b/c**, **a**, **b**, and **c** respectively represents a layer.                | No                    |
      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+
      | User Application        | Name of a user application.                                                                                                                                                                                                                                                                                  | Yes                   |
      +-------------------------+--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------+

.. |image1| image:: /_static/images/en-us_image_0000001737607793.png
