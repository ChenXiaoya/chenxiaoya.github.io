---
title: MySQL 数据类型
---

在 MySQL 中，有三种主要的类型：文本、数字和日期/时间类型。
>Text 类型：
CHAR(size)
VARCHAR(size)
TINYTEXT
TEXT
BLOB
MEDIUMTEXT
MEDIUMBLOB
LONGTEXT
LONGBLOB
ENUM(x,y,z,etc.)
SET

>Number 类型：
TINYINT(size):-128 到 127 常规。0 到 255 无符号*。在括号中规定最大位数
SMALLINT(size):-32768 到 32767 常规。0 到 65535 无符号*。在括号中规定最大位数。
MEDIUMINT(size):-8388608 到 8388607 普通。0 to 16777215 无符号*。在括号中规定最大位数。
INT(size):-2147483648 到 2147483647 常规。0 到 4294967295 无符号*。在括号中规定最大位数。
BIGINT(size):-9223372036854775808 到 9223372036854775807 常规。0 到 18446744073709551615 无符号*。在括号中规定最大位数。
FLOAT(size,d):带有浮动小数点的小数字。在括号中规定最大位数。在 d 参数中规定小数点右侧的最大位数。
DOUBLE(size,d):带有浮动小数点的大数字。在括号中规定最大位数。在 d 参数中规定小数点右侧的最大位数。
DECIMAL(size,d):作为字符串存储的 DOUBLE 类型，允许固定的小数点。

* 这些整数类型拥有额外的选项 UNSIGNED。通常，整数可以是负数或正数。如果添加 UNSIGNED 属性，那么范围将从 0 开始，而不是某个负数。


