:original_name: apm_07_0034.html

.. _apm_07_0034:

Access Keys
===========

Access Key ID (AK) and Secret Access Key (SK) are your long-term identity credentials. JavaAgents report data with an AK. An AK is used together with an SK to sign requests cryptographically, ensuring that the requests are secret, complete, and correct.

Precautions
-----------

A user can create a maximum of two access keys with identical permissions and unlimited validity. Keep your access keys secure and change them periodically for security purposes. To change an access key, delete it and create a new one.

APM allows you to encrypt and decrypt the SK in the **apm.config** file.

The encryption and decryption process is as follows:

#. Compile a Java class, for example, **com.demo.DecryptDemo**, and add a decryption method, for example, decrypt both the input and output to character strings.

#. Compile the decryption method to decrypt the SK and return the decrypted value.

#. Pack the **com.demo.DecryptDemo** class into a JAR package and place this JAR package and its dependent packages in the **apm-javaagent/ext** folder of JavaAgent.

#. Add the following content to the **apm.config** file:

   **decrypt.className=com.demo.DecryptDemo**

   **decrypt.methodName=decrypt**

   **secret.key={**\ *Character string encrypted by users*\ **}**

Adding an Access Key
--------------------

#. Log in to the management console.

#. Click |image1| on the left and choose **Application** > **Application Performance Management**.

#. In the navigation pane, choose **System Management** > **Access Keys**.

#. On the page that is displayed, click **Add Access Key**.


   .. figure:: /_static/images/en-us_image_0000001943060937.png
      :alt: **Figure 1** Adding an AK/SK

      **Figure 1** Adding an AK/SK

#. Add an access key description and click **Yes** to generate an access key.

   To modify the description, click **Modify** in the **Operation** column in the row that contains the target access key.

Deleting an Access Key
----------------------

#. In the navigation pane, choose **System Management** > **Access Keys**.
#. On the **Access Keys** page, locate the row that contains the target access key and click **Delete** in the **Operation** column.
#. On the page that is displayed, click **Yes** to delete the access key.

Enabling or Disabling an Access Key
-----------------------------------

Each access key is enabled by default. To disable it, do as follows:

#. In the navigation pane, choose **System Management** > **Access Keys**.

#. On the **Access Keys** page, locate the row that contains the target access key and click **Disable** in the **Operation** column.

#. On the page that is displayed, click **Yes** to disable the access key.

   To enable it again, click **Enable** in the row that contains the access key. On the page that is displayed, click **Yes**.

.. |image1| image:: /_static/images/en-us_image_0000001908301692.png
