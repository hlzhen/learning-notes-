# Mysql相关概念

## 1.数据库对象
```markdown
# 数据库对象是数据库的组成部分，常见的有如下几种
  ## 表(Table） 
    . 数据库中的表与我们日常生活中使用的表格类似，它也是由 `行(Row)` 和 `列(Column)` 组成的。
    . 列(Column)由 `同类` 的信息组成，每列又称为一个字段，每列的标题称为字段名。
    . 行(Row)包括了 `若干列` 信息项。一行数据称为一个或一条记录，它表达有一定意义的信息组合。
    . 一个数据库表由一条或多条记录组成，没有记录的表称为空表。每个表中通常都有一个主关键字，用于惟一地确定一条记录。
  ## 索引(Index)
    . 索引是根据指定的数据库表列建立起来的 `顺序`。
    . 它提供了 `快速访问数据` 的途径，并且可 `监督表的数据`，使其索引所指向的列中的 `数据不重复`。
  ## 视图(View)
    . 视图看上去同表似乎一模一样，具有一组命名的字段和数据项，但它其实是一个 `虚拟` 的表，在数据库中并不实际存在。
    . 视图是由 `查询数据库表` 产生的，它限制了用户能看到和修改的数据。
    . 由此可见，视图可以用来控制用户对数据的访问，并能简化数据的显示，即通过视图只显示那些需要的数据信息。
  ## 图表(Diagram)
    . 图表其实就是数据库表之间的关系示意图。利用它可以编辑表与表之间的关系。
  ## 缺省值(Default)
    . 缺省值也叫`默认值`是当在表中创建列或插入数据时，对没有指定其具体值的列或列数据项赋予事先设定好的值。
  ## 规则(Rule) 
    . 规则是对数据库表中数据信息的限制。它 `限定的是表的列` 。
  ## 触发器(Trigger)
    . 触发器是一个用户定义的SQL事务命令的集合。
    . 当对一个表进行插入、更改、删除时，这组命令就会 `自动执行`，前提是满足这个触发器的条件。
  ## 存储过程(Stored Procedure)
    . `存储过程是为完成特定的功能而汇集在一起的一组SQL程序语句，经编译后存储在数据库中的SQL程序`。
  ## 用户(User)
    1. 所谓用户就是有权限访问数据库的人。

```


## 2. DB、DBMS、SQL之间的关系
```markdown
# BD
 . 数据库(database)，用于存储结构化的数据，在硬盘上以文件的形式存在。

# DBMS
 . 数据库管理系统(database management system)，常见的有Mysql、Oracle、DB2、SqlServer等等。

# SQL
 . 结构化查询语言，是一门标准的通用语言。
 . SOL就是能让用户和关系型數据库进行交互的一种语言

# 三者之间的关系
 . DBMS -(执行)-> SQL -(操作)-> DB
```

## 3. SQL分类
```markdown
# DDL(Data Definition Language) - 数据定义语言
 . 可以创建与修改数据库本身。关键字如下：
 . create
 . alter
 . drop
 . rename 
 . truncate
# DML(Data Manipulation Language) - 数据操作语言
 . 可以对数据库中的数据进行增、删、改、查操作。关键字如下
 . insert
 . delete 
 . update
 . select
# DCL(Data Control Language) - 数据控制语言
 . 用于维护数据库操作的安全性。关键字如下：
 . commit
 . rollback
 . savepoint
 . grant
 . revoke

 `注意`: 
  . DQL(Data Query Language)- 数据查询语言 其实是 数据操作语言的一种分支也可以看作是一种分类
  . TCL(Transaction Control Language) - 事物控制语言 也是 数据控制语言的一种分支也可以看作是一种分类
```

## 4.函数
```markdown
# 什么是函数？
1. 一组预先编译好的SQL语句的集合，理解成批处理语句
2. 换句话说，函数就好比我们开发中把经常使用的代码封装起来，需要时可直接调用。

# 函数的作用
1. 提高代码的效率与维护性
2. 简化操作
```