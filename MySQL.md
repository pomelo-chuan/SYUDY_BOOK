MySQL
---

## 一、

1. **数据库（database）**：保存有组织数据的容器


2. **表（table）**：某种特定类型的数据的结构化清单。


3. **模式（schema）**：关于数据库和表的布局及特性的信息。


> 表由列组成，列中存储着表中某部分的信息。

4. **列（column）**：表中的一个字段。所有表都是由一个或者多个列组成的。


> 数据库中每个列都有相应的数据类型。

5. **数据类型（datatype）**：允许的数据的类型。


> 表中的数据是按行存储的，所保存的记录存储在自己的行内。

6. **行（row）**：表中的一个记录


7. **主键（primary key）**：一列（或者一组列），其值能够唯一区分表中的每个行。

主键需要满足的条件：

* 任意两行不可有相同的主键值
* 每行必须有一个主键值（主键列不允许有NULL值）

## 二、MySQL

1. 客户机 - 服务器软件

DBMS可分为两类：
* 基于共享文件系统的DBMS
* 基于客户机 - 服务器的DBMS


