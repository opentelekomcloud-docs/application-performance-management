:original_name: apm_07_0013.html

.. _apm_07_0013:

Configuring the MySQL Monitoring Item
=====================================

On the **Modify MySQL Monitoring Configuration** page, set the following parameters:

-  **Collection Interval**: The default value is **60s** and cannot be changed.
-  **Collect Original SQL**: This function is disabled by default. In that case, only SQL statements without values are collected, for example, **select name from user where id=?**. When this function is enabled, SQL statements with values are collected, for example, **select name from user where id=1**.
-  **shardTableName**: specified when you need to aggregate multiple tables into one table. For example, there are two tables: **UserTable_1** and **UserTable_2**. By default, two SQL statements (**select name from UserTable_1** and **select name from UserTable_2**) are displayed on the SQL monitoring page. If you set **shardTableName** to **UserTable**, tables starting with **UserTable** are aggregated into the same table. Only one SQL statement (**select name from UserTable**) is displayed on the SQL monitoring page.
-  **mysqlMaxRows**: the maximum number of MySQL rows that can be collected by the Agent. If this value has been reached, the Agent stops collecting data immediately. The default value is **500**. The value ranges from 10 to 2000.
-  **sqlSize**: the maximum number of SQL statement bytes that can be collected by the Agent. Only when the number of bytes is within **sqlSize**, can SQL statements be collected. The default value is **2000**. The value ranges from 10 to 4096.


.. figure:: /_static/images/en-us_image_0000001676082137.png
   :alt: **Figure 1** Configuring the MySQL monitoring item

   **Figure 1** Configuring the MySQL monitoring item
