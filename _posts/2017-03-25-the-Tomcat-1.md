---
title: Tomcat配置
layout: post
date: '2017-03-25 15:49:12 +0800'
categories: tomcat
---


一、**tomcat安装文件目录**

bin: 可执行文件

conf ：xml配置文件

lib: 使用的库

logs：日志

temp:

webapps: 部署位置

work: 编译后产生的临时文件。


二、**配置**

要想启动Tomcat，需要配置两个环境变量(注：环境变量的位置---"右键我的电脑-属性-高级系统设置-高级-环境变量")

1）JAVA_HOME:值为JDK的安装目录（例：C:\Program Files (x86)\Java\jdk1.7.0_55）

2）CATALINA_HOME:值我Tomcat的安装目录（例：D:\apache-tomcat-8.5.11）

验证：打开IE 输入： http://localhost:8080 。 出现小猫的网页就成功了。

**Eclipse配置tomcat**

在tomcat安装目录的conf目录下打开server.xml文件，找到倒数第四行`</Host>`，在它的上面添加下面代码

```xml
<Context path="上下文路径" docBase="webroot路径" reloadable="true" />
```

验证：http://localhost:8080/test/login.jsp 正常显示说明成功。

