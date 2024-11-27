:original_name: apm_07_0208.html

.. _apm_07_0208:

Introduction
============

APM has a built-in CMDB for managing application structure information and related configurations. It involves the following concepts:

-  **Application** (global concept): a logical unit. An application can be an independent functional module. The same application information can be viewed in all regions.
-  **Sub-application** (global concept): similar to a folder. There can be up to three layers of sub-applications under an application.
-  **Component** (global concept): a program or microservice. It is generally used together with environments. It may contain one or more environments. For example, an order app can be deployed in the function test environment, pressure test environment, pre-release environment, or live network environment.
-  **Environment**: Components or programs with different configurations are deployed in different environments. Each environment has its own region attribute. You can filter environments by region. You can also add one or more tags to an environment and filter environments by tag.
-  **Instance**: a process in an environment. It is named in the format of "host name+IP address+instance name". An environment is usually deployed on different hosts or containers. If an environment is deployed on one host, differentiation by instance is supported.
-  **Environment tag**: an attribute for filtering environments. Different environments may have the same tag. Tags carry public configuration capabilities. For example, the configuration set on a tag can be shared by the environments with the same tag. Tags defined for environments of one application cannot be applied to other applications.

The following shows an example of the CMDB structure.


.. figure:: /_static/images/en-us_image_0000001934305448.png
   :alt: **Figure 1** CMDB structure

   **Figure 1** CMDB structure

The CMDB structure tree can be hidden.

#. Click **Hide** to hide the CMDB structure tree.


   .. figure:: /_static/images/en-us_image_0000001961504785.png
      :alt: **Figure 2** Hiding the CMDB structure tree

      **Figure 2** Hiding the CMDB structure tree

#. Go to the path above in the upper part of the page and select your target node.


   .. figure:: /_static/images/en-us_image_0000001934305460.png
      :alt: **Figure 3** Selecting a node

      **Figure 3** Selecting a node

#. Click **Expand** to display the CMDB structure tree.
