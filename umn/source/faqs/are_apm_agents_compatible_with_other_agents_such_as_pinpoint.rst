:original_name: apm_03_0001.html

.. _apm_03_0001:

Are APM Agents Compatible with Other Agents Such as Pinpoint?
=============================================================

No.

Generally, APM implements bytecode instrumentation based on the ASM framework. Installing two Agents means two instrumentation operations on your code. Code instrumentation mechanisms vary according to products. If you install Agents of different products, code conflicts may occur, affecting performance.

Therefore, do not install APM Agents together with other Agents.
