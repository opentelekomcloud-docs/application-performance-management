:original_name: apm_07_0014.html

.. _apm_07_0014:

Configuring the HttpClient Monitoring Item
==========================================

On the **Modify HttpClient Monitoring Configuration** page, set the following URL normalization parameters:

-  **Collection Interval**: The default value is **60s** and cannot be changed.
-  URL normalization is used to aggregate URLs that meet the conditions you set. For example, **http://localhost/rest/v1/test/123** and **http://localhost/rest/v1/test/234** can be aggregated into **http://localhost/rest/v1/test/**\ *{id}*.
-  **httpClientMaxRows**: the maximum number of HttpClient rows that can be collected by the Agent. If this value has been reached, the Agent stops collecting data immediately. The default value is **500**. The value ranges from 10 to 2000.

.. _apm_07_0014__en-us_topic_0000001217131578_fig78581952152820:

.. figure:: /_static/images/en-us_image_0000001676203089.png
   :alt: **Figure 1** Configuring the HttpClient monitoring item

   **Figure 1** Configuring the HttpClient monitoring item

.. _apm_07_0014__en-us_topic_0000001217131578_section195174419328:

Normalization Methods
---------------------

There are four normalization methods: **Startwith**, **Endwith**, **Include**, and **Regex**.

-  **Startwith**: URLs starting with a certain expression are counted as normalized URLs. For example, URLs starting with **http://127.0.0.1/v1** are aggregated into **/v1/test/**\ *{id}*, as shown in :ref:`Figure 1 <apm_07_0014__en-us_topic_0000001217131578_fig78581952152820>`.

-  **Endwith**: URLs ending with a certain expression are counted as normalized URLs. For example, URLs ending with **/test** are aggregated into **/**\ *{id}*\ **/test**, as shown in :ref:`Figure 1 <apm_07_0014__en-us_topic_0000001217131578_fig78581952152820>`.

-  **Include**: URLs containing a certain expression are counted as normalized URLs. For example, URLs containing **test** are aggregated into **/test/**\ *{id}*, as shown in :ref:`Figure 1 <apm_07_0014__en-us_topic_0000001217131578_fig78581952152820>`.

-  **Regex**: URLs that meet the wildcard expression are counted as normalized URLs. For details about the wildcard rules, see :ref:`Table 1 <apm_07_0014__en-us_topic_0000001217131578_table697071013715>`.

   .. _apm_07_0014__en-us_topic_0000001217131578_table697071013715:

   .. table:: **Table 1** Wildcard description

      ======== =======================================
      Wildcard Description
      ======== =======================================
      ?        Matches any character.
      \*       Matches zero, one, or more characters.
      \*\*     Matches zero, one, or more directories.
      ======== =======================================

Usage Example
-------------

The following is an example:

+-------------------------+-------------------------------------------------------------------------------------------------------------------+
| URL Path                | Description                                                                                                       |
+=========================+===================================================================================================================+
| /app/p?ttern            | Matches files such as **/app/pattern** and **/app/pAttern**, excluding **/app/pttern**.                           |
+-------------------------+-------------------------------------------------------------------------------------------------------------------+
| /app/``*``.x            | Matches all **.x** files in the **app** directory.                                                                |
+-------------------------+-------------------------------------------------------------------------------------------------------------------+
| /``**``/example         | Matches **/app/example**, **/app/foo/example**, and **/example**.                                                 |
+-------------------------+-------------------------------------------------------------------------------------------------------------------+
| /app/``**``/dir/file.\* | Matches **/app/dir/file.jsp**, **/app/foo/dir/file.htm**, **/app/foo/bar/dir/file.pdf**, and **/app/dir/file.c**. |
+-------------------------+-------------------------------------------------------------------------------------------------------------------+
| ``/**/*``.jsp           | Matches all **.jsp** files.                                                                                       |
+-------------------------+-------------------------------------------------------------------------------------------------------------------+
