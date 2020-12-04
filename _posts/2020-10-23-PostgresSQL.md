### 对比mysql pgsql
[原文](https://blog.csdn.net/u012414189/article/details/84064146)
一.PostgreSQL相对于MySQL的优势
1、在SQL的标准实现上要比MySQL完善，而且功能实现比较严谨；
2、存储过程的功能支持要比MySQL好，具备本地缓存执行计划的能力；
3、对表连接支持较完整，优化器的功能较完整，支持的索引类型很多，复杂查询能力较强；
4、PG主表采用堆表存放，MySQL采用索引组织表，能够支持比MySQL更大的数据量。
5、PG的主备复制属于物理复制，相对于MySQL基于binlog的逻辑复制，数据的一致性更加可靠，复制性能更高，对主机性能的影响也更小。
6、MySQL的存储引擎插件化机制，存在锁机制复杂影响并发的问题，而PG不存在。

二、MySQL相对于PG的优势：
1、innodb的基于回滚段实现的MVCC机制，相对PG新老数据一起存放的基于XID的MVCC机制，是占优的。新老数据一起存放，需要定时触 发VACUUM，会带来多余的IO和数据库对象加锁开销，引起数据库整体的并发能力下降。而且VACUUM清理不及时，还可能会引发数据膨胀；
2、MySQL采用索引组织表，这种存储方式非常适合基于主键匹配的查询、删改操作，但是对表结构设计存在约束；
3、MySQL的优化器较简单，系统表、运算符、数据类型的实现都很精简，非常适合简单的查询操作；
4、MySQL分区表的实现要优于PG的基于继承表的分区实现，主要体现在分区个数达到上千上万后的处理性能差异较大。
5、MySQL的存储引擎插件化机制，使得它的应用场景更加广泛，比如除了innodb适合事务处理场景外，myisam适合静态数据的查询场景。

三、总结
开源数据库都不是很完善，商业数据库oracle在架构和功能方面都还是完善很多的。从应用场景来说，PG更加适合严格的企业应用场景（比如金融、电信、ERP、CRM），而MySQL更加适合业务逻辑相对简单、数据可靠性要求较低的互联网场景（比如google、facebook、alibaba）。