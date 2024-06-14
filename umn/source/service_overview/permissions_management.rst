:original_name: apm_01_0007.html

.. _apm_01_0007:

Permissions Management
======================

If you need to assign different permissions to employees in your enterprise to access your APM resources, Identity and Access Management (IAM) is a good choice for fine-grained permissions management. IAM provides identity authentication, permissions management, and access control, helping you secure access to your cloud resources.

With IAM, you can use your account to create IAM users for your employees, and assign permissions to the users to control their access to specific resources. For example, some software developers in your enterprise need to use APM resources but cannot delete them or perform any high-risk operations. To achieve this result, you can create IAM users for the software developers and grant them only the permissions required for using APM resources.

If your account does not need individual IAM users for permissions management, you may skip over this chapter.

IAM can be used free of charge. You pay only for the resources in your account. For more information about IAM, see `IAM Service Overview <https://docs.otc.t-systems.com/identity-access-management/umn/service_overview/what_is_iam.html#iam-01-0026>`__.

.. _apm_01_0007__en-us_topic_0000001195725122_section186901838201416:

APM Permissions
---------------

By default, new IAM users do not have any permissions assigned. You need to add a user to one or more groups, and assign permissions policies or roles to these groups. The user then inherits permissions from the groups it is a member of. This process is called authorization. After authorization, the user can perform specified operations on APM.

APM is a global service. By default, the APM permissions granted to a user take effect in all regions supported by APM. APM resources are isolated by tenant. All users under a tenant share resources. To isolate resources, use enterprise projects.

APM is a global service and can be accessed without specifying a physical region.

:ref:`Table 1 <apm_01_0007__en-us_topic_0000001195725122_table7749356973>` lists all the system permissions supported by APM.

.. _apm_01_0007__en-us_topic_0000001195725122_table7749356973:

.. table:: **Table 1** System permissions supported by APM

   ================== ============================= =====================
   Role               Description                   Category
   ================== ============================= =====================
   APM FullAccess     Full permissions for APM      System-defined policy
   APM ReadOnlyAccess Read-only permissions for APM System-defined policy
   ================== ============================= =====================

:ref:`Table 2 <apm_01_0007__en-us_topic_0000001195725122_table1153711211269>` lists the common operations supported by each system-defined policy or role of APM. Choose policies or roles as required.

.. _apm_01_0007__en-us_topic_0000001195725122_table1153711211269:

.. table:: **Table 2** Common operations supported by each system-defined policy or role of APM

   =================================== ============== ==================
   Operation                           APM FullAccess APM ReadOnlyAccess
   =================================== ============== ==================
   Querying the alarm list             Y              Y
   Querying alarm details              Y              Y
   Querying alarm notification details Y              Y
   Obtaining application configuration Y              Y
   Creating application configuration  Y              x
   Deleting application configuration  Y              x
   Modifying application configuration Y              x
   Querying a tag                      Y              Y
   Adding a tag                        Y              x
   Deleting a tag                      Y              x
   Modifying a tag                     Y              x
   Querying an alarm template          Y              Y
   Adding an alarm template            Y              x
   Deleting an alarm template          Y              x
   Modifying an alarm template         Y              x
   Obtaining a notification            Y              Y
   Deleting a notification             Y              x
   Adding a notification               Y              x
   Modifying a notification            Y              x
   Obtaining URL tracing configuration Y              Y
   Deleting URL tracing configuration  Y              x
   Adding a URL for tracing            Y              x
   Modifying URL tracing configuration Y              x
   Querying a URL tracing view         Y              Y
   Obtaining the URL tracing list      Y              Y
   Obtaining the global topology       Y              Y
   Querying a sub-application          Y              Y
   Querying environment configuration  Y              Y
   Adding environment configuration    Y              x
   Deleting environment configuration  Y              x
   Modifying environment configuration Y              x
   Obtaining an instance               Y              Y
   Deleting an instance                Y              x
   Modifying an instance               Y              x
   Querying a monitoring item          Y              Y
   Modifying a monitoring item         Y              x
   Obtaining collection status         Y              Y
   Obtaining a custom alarm policy     Y              Y
   Deleting a custom alarm policy      Y              x
   Modifying a custom alarm policy     Y              x
   Creating a custom alarm policy      Y              x
   Obtaining the environment topology  Y              Y
   Obtaining a metric view             Y              Y
   Obtaining the trace list            Y              Y
   Obtaining trace details             Y              Y
   Obtaining collector information     Y              Y
   Obtaining an access key             Y              x
   Modifying an access key             Y              x
   Deleting an access key              Y              x
   Adding an access key                Y              x
   Obtaining general configuration     Y              Y
   Modifying general configuration     Y              x
   Querying Agent statistics           Y              Y
   =================================== ============== ==================
