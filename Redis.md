# Redis



# ==过渡==

# 1.Nosql介绍

- NOSQL(not only SQL 不仅仅是数据库)非关系数据库

- 方便扩展，数据之间没有关系

- 不需要事先设计数据库

- 本质上是一个内存的key-value缓存这个没什么好说的，这是nosql数据库的标准特点

  

**为什么要用Nosql：**

​	发展过程： **优化数据结构和索引--> 文件缓存（IO）---> Memcached（高性能的、具有分布式内存对象的缓存系统）**



早些年MyISAM ：实现了表锁，当我查询一条数据的时候，所把整个表锁起来，不利于高并发

转战为InnoDB : 实现了行锁



Nosql的分类：

1. KV键值对数据库 。有：`redis`（c语言编写）**、memecache、tair** (应用于内容缓存、处理大数据量的高访问负载、日志等
   查找速度快但是数据无结构化 )

2. 文档型数据库 。有：**ConthDB、`MongoDB` （**基于分布式文件存储的数据库，C++编写，主要用于处理大量文档；它是一种介于关系型数据库和非关系型数据库的中间产品，是nosql中功能最丰富、最像关系型数据库的非关系型数据库）
   应用于web应用
   数据结构要求不严格、表结构可变、不需要预定义表结构但查询性能不高且缺少统一查询语言)

3. 列存储数据库
   **`HBase`（大数据）、Cassandra**
   应用于分布式文件系统
   查找速度快、可扩展性强但功能相对局限

4. 图关系数据库（不是存图形，而是存关系，比如：朋友圈、社交网络、广告推荐）
   **`Neo4j`、InfoGrid**
   应用于社交网络、推荐系统
   可以利用图结构相关的算法但是计算时需要全部图，导致不太好做分布式集群

   

   

   ``