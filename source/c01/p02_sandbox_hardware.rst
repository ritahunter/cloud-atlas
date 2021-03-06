================================
1.2 沙箱环境的硬件选型
================================

--------------------
我的初步硬件方案
--------------------

目前我个人有两台旧笔记本电脑模拟IDC云计算基础服务器
  * ThinkPad X220 （约2011年产品）, i5-2410M CPU @ 2.30GHz, 8G 内存，512G SSD磁盘
  * MacBook Air（约2014年产品）, i5-4260U CPU @ 1.40GHz, 8G 内存, 128G SSD磁盘

树莓派：
  * 3个三代树莓派通过扩展卡连接SATA笔记本硬盘，作为Ceph存储的基础

.. note::

  树莓派并非性能强劲的硬件，目前主要是为了验证自己一个关于在ARM硬件平台运行计算集群的想法。你可以不使用树莓派。

.. note::

  已上硬件选型主要是为了利旧，并非最合适作为沙箱环境的硬件选型。但是，我依然在本书中采用这样的硬件，是为了证明，即使是几年前淘汰的硬件(分别是6年前和3年前)，依然能够帮助我们学习最新的云计算技术。

--------------------
可能更好的硬件方案
--------------------

如果可以投入更多的资金，我发现可能选择二手服务器来组建个人学习云计算平台更为合适。

在淘宝上有淘汰下来的二手服务器，配置上硬盘和内存，实现基于分布式存储的底层，同时基于Xeon强大的多核硬件平台，配置尽可能高的内存，理论上可以模拟出极大规模的数据中心。

让我们来估算一下成本：

* 二手Dell  2台
* 硬盘（4T规格） 3个 x 2 
* 内存（最好为服务器满配，因为能够运行的虚拟机数量主要取决于内存）

.. note::

  请采用能够负担的最大容量硬盘和最大容量的内存：在沙箱环境中，由于需要在单机上模拟大量的服务器，最主要的资源需求是内存，其次是硬盘。