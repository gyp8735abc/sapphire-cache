# SapphireCache简介 #

SapphireCache是一个高并发、高缓存吞吐性、高性能的企业级Java分布式内存对象缓存系统，其具有简单易学、方便实用等特点。它能够用来存储各种格式的数据，包括图像、视频、文件以及数据库检索的结果等。简单的说就是将数据源中的数据临时存储于内存中，然后从内存中读取，从而大大提高读取速度.

当然SapphireCache不仅仅是一个缓存系统，您还可以使用它为你构建复杂的企业级集群应用。SapphireCache可以充分挖掘您物理机器的可用资源，将性能提升至极限,这便是Sapphire能带给您的服务。


## 为何使用SapphireCache ##

确实目前开源环境中拥有广泛的缓存系统，为何您还需要您使用SapphireCache。我们相信如下2点将会带给您所需要的答案：


  * 超轻量级、实现企业极速开发；

  * 封装层次极低，减少不必要的资源频率开销；



## SapphireCache与EhCache性能对比 ##

为了达到一个公平客观的测试结果，SapphireCache与EhCache均选用相同的测试环境及测试方案。关于测试方案我们将测试SapphireCache与EhCache在本地缓存CRUD操作性上的性能差异。
但是由于SapphireCache的发布版本都是开启了缓存内存计算的，所以在资源消耗比EhCache要大一些。

下图为开启缓存内存计算的SapphireCache与EhCache本地缓存CRUD操作的性能对比：
![http://dl.iteye.com/upload/picture/pic/117335/c584abc5-ce05-374d-a49a-724077df5ed9.jpg](http://dl.iteye.com/upload/picture/pic/117335/c584abc5-ce05-374d-a49a-724077df5ed9.jpg)

下图为关闭缓存内存计算的SapphireCache与EhCache本地缓存CRUD操作的性能对比：
![http://dl.iteye.com/upload/picture/pic/117339/29af3389-e8c5-3fb8-926c-da1932a53e59.jpg](http://dl.iteye.com/upload/picture/pic/117339/29af3389-e8c5-3fb8-926c-da1932a53e59.jpg)

经过上图大家可以发现，SapphireCache一旦关闭缓存内存计算后其实和EhCache的本地CRUD操作性能差异不大，如果稍加优化，SapphireCache甚至可以超越EhCache的本地缓存CRUD操作性。


## SapphireCache最新版本 ##

SapphireCache目前最新版本为1.2.0-BETA, 主要特性包含：

  * 敏捷快速；

  * 体系结构中立，跨平台支持；

  * 多种缓存管理容器实现；

  * 多种缓存回收策略（LRU、LFU、FIFO、RDM）；

  * 支持缓存注解服务驱动（Annotation方式直接缓存方法）；

  * 支持缓存持久化及加载虚拟机运行期数据；

  * 单个缓存最大缓存容量为1gByte；

  * 支持缓存容量单位设置（byte、kByte、mByte、gByte）；

  * 支持TCP单播集群（BIO/NIO）、P2P广播、组播集群、RMI组播集群；


## SapphireCache与EhCache、MemCache功能比较 ##

|功能|SapphireCache|EhCache|MemCache|
|:-|:------------|:------|:-------|
|平台无关性|支持           |支持     |不完全     |
|封装层次|极低           |低      |中       |
|资源开销率|低            |低      |低       |
|分布式|支持           |支持     |不完全，集群默认不实现|
|缓存持久化|支持           |支持     |缺省不支持   |
|加载虚拟机运行期数据|支持           |支持     |不支持     |
|缓存并发性能|高            |高      |高       |
|缓存吞吐性能|高            |高      |中       |
|容灾|不支持          |支持     |支持      |
|缓存数据方式|内存及磁盘        |内存及磁盘  |内存中     |
|缓存回收策略|LRU、LFU、FIFO、RDM|LRU、LFU、FIFO|LRU     |
|Annotations服务|支持           |不支持，由Spring实现|缺省不支持，由Spring实现|
|代码侵入性|极低           |低      |低       |
|开源性|完全           |完全     |不完全     |


## SapphireCache快速入门 ##

  * SapphireCache的API文档 [点击查看](http://code.google.com/p/sapphire-cache/wiki/SapphireCacheAPI)

  * 使用SapphireCache构建基础缓存架构 [点击查看](http://code.google.com/p/sapphire-cache/wiki/UseSapphire?ts=1342947132&updated=UseSapphire)