:original_name: apm_07_0017.html

.. _apm_07_0017:

Monitoring Item Views
=====================

APM supports summary tables, trend graphs, latest data tables, and original data tables.

-  Summary table: records the summary calculation results based on the primary key metric within a period. You can click a number or character string in the summary table to view the trend graph of the primary key metric.
-  Trend graph: displays the trend of a primary key metric in a period. A trend graph may have breakpoints, indicating that no data is collected in this period. There are multiple reasons why data is not collected. For example, collectors do not collect the metrics with zero calls or the data may be lost.
-  Original data table: For character strings, no trend graphs can be generated. Therefore, original data tables are used. Each row indicates the mapping between a time and a value.
-  Latest data table: displays the latest data. You can click a data record to view its trend graph.

.. note::

   The view of each monitoring item is configured in the background and has not been opened. You can check views together with corresponding background metric sets. For details, see :ref:`Metric Sets <apm_07_0031__en-us_topic_0000001087028667_section2697316421>`.
