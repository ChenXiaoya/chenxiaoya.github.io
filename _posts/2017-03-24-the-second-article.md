---
title: SQL基础
---

一、创建数据库
> creat创建
```
CREATE DATABASE databasename;
例：
CREATE DATABASE testDB;
```

二、创建表
> creat创建
```
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
   ....
);
例：
CREATE TABLE Persons (
    PersonID int,
    LastName varchar(255),
    FirstName varchar(255),
    Address varchar(255),
    City varchar(255) 
);
```

三、删除
>drop删除数据库或表
```
DROP DATABASE databasename;
DROP TABLE table_name;
```

四、查询选择
>使用select、from、where关键字
```
 SELECT 列名称 FROM 表名称 WHERE 列 运算符 值
 例：
 SELECT * FROM Persons WHERE City='Beijing'
```

五、排序
>reader by 语句用于根据指定的列对结果集进行排序。默认按照升序对记录进行排序。如果您希望按照降序对记录进行排序，可以使用 DESC 关键字。
```
例：
以字母顺序显示公司名称：
SELECT Company, OrderNumber FROM Orders ORDER BY Company
以逆字母顺序显示公司名称：
SELECT Company, OrderNumber FROM Orders ORDER BY Company DESC
```

六、向表格中插入新的行
>instert into语句用于向表格中插入新的行。
```
例：
INSERT INTO Persons (LastName, Address) VALUES ('Wilson', 'Champs-Elysees')
```

七、更新表中的数据
>update...set... 语句用于修改表中的数据。
```
我们为 lastname 是 "Wilson" 的人添加 firstname：
UPDATE Person SET FirstName = 'Fred' WHERE LastName = 'Wilson' 
```

八、删除表中的行
>delete 语句用于删除表中的行
```
例：
DELETE FROM Persons WHERE LastName = 'Wilson' 
```
九、引号的使用

>SQL 使用单引号来环绕文本值（大部分数据库系统也接受双引号）。如果是数值，请不要使用引号。
```
例：
文本值：
SELECT * FROM Persons WHERE FirstName='Bush'
数值：
SELECT * FROM Persons WHERE Year>1965
```


