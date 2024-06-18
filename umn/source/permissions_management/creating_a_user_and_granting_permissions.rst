:original_name: apm_07_0038.html

.. _apm_07_0038:

Creating a User and Granting Permissions
========================================

This chapter describes how to use IAM for fine-grained permissions control for your APM resources. With IAM, you can:

-  Create IAM users for employees based on your enterprise's organizational structure. Each IAM user will have their own security credentials for accessing APM resources.
-  Manage permissions on a principle of least permissions (PoLP) basis.
-  Entrust an account or cloud service to perform efficient O&M on your APM resources.

If your account does not need individual IAM users, skip this chapter.

This section describes the procedure for granting permissions (see :ref:`Figure 1 <apm_07_0038__en-us_topic_0000001088190833_fig132391629233>`).

Prerequisite
------------

Learn about the permissions supported by APM and choose policies or roles based on your requirements. For details, see :ref:`Permissions Management <apm_01_0007__en-us_topic_0000001195725122_section186901838201416>`.

Process Flow
------------

**Supported Cloud Services**

.. _apm_07_0038__en-us_topic_0000001088190833_fig132391629233:

.. figure:: /_static/images/en-us_image_0000001218178520.png
   :alt: **Figure 1** Process for granting APM permissions

   **Figure 1** Process for granting APM permissions

#. .. _apm_07_0038__en-us_topic_0000001088190833_li1682215710191:

   `Creating a User Group and Assigning Permissions <https://docs.otc.t-systems.com/identity-access-management/umn/user_guide/user_groups_and_authorization/creating_a_user_group_and_assigning_permissions.html#en-us-topic-0046611269>`__

   Create a user group on the IAM console, and assign the **APM ReadOnlyAccess** policy to the group.

#. `Creating a User <https://docs.otc.t-systems.com/identity-access-management/umn/user_guide/iam_users/creating_a_user.html#en-us-topic-0046611303>`__

   Create a user on the IAM console and add the user to the group created in :ref:`1 <apm_07_0038__en-us_topic_0000001088190833_li1682215710191>`.

#. `Logging In as an IAM User <https://docs.otc.t-systems.com/identity-access-management/umn/user_guide/iam_users/logging_in_as_an_iam_user.html>`__ and Verifying Permissions

   Log in to the APM console using the created user, and verify that the user only has read permissions for APM.
