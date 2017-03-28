---
title: 反射
layout: post
date: '2017-03-27'
categories: Reflection
---
前言：

本文根据圣思园张龙的视频和搜索的反射资料做的笔记

## JAVA 语言的反射机制

# 一、反射提供了以下几个功能

1. 在运行时，判断任意一个对象所属的类。
2. 在运行时，构造任意一个类的对象。
3. 在运行时，判断任意一个类所具有的成员变量和方法
4. 在运行时，判断任意一个对象的方法

# 二、反射的操作

**1.要想使用反射，首先需要获得待处理类或者对象所对应的Class对象。**

**2.获取某个类或者某个对象所对应的Class对象的常用的3中方式：**

* 使用Class类的静态方法forName：`Class.forName("java.lang,String")``;
* 使用类的.class语法：` String.class;`
* 使用对象的getClass()方法：`String s = "aa";` `Class<?> clazz = s.getClass();`

**3.要想通过类的**不带参数**的构造方法来生成对象，我们有两种方式：**

1) 先获得Class对象， 然后通过该Class对象的`newInstance()`方法直接生成即可：

```java
Class<?> classType = string.class;
Object obj = classType.newInstance();
```

2) 先获得Class对象，然后通过该对象获得对应的Constructor对象，再用过该Constructor对象的`newInstance()`方法生成。

```java
Class<?> classType = Customer.class;
Constructor cons = classType.getConstructor(new Class[]{});
Object obj = cons.newInstance(new Object[]{});
```

**4.若想要通过类的**带参数**的构造方法生成对象，只能使用下面的方式:**

```java
Constructor cons = classType.getConstructor(new Class[]{String.class,
int.class});
Object obj = cons.newInstance(new Object[]{"hello"});
```

**5.Integer.TYPE 与 Integer.class 的区别**

构造数组时，打印`Integer.TYPE`返回的时原生类型`int`.

打印`Integer.class`返回的时integer类所对象的class对象。即，`class java.lang.Integer`.

# 三、实现反射机制的类

在JDK中，主要由一下类来实现Java的发射机制，这些类都存在于java.lang.reflect包中。

类名|描述
-|-
Class类|类
Field类|类成员变量，即类的属性
Method类|类的方法
Constructor类|类的构造方法
Array类|提供了动态创建数组，以及访问数组的元素的静态方法。