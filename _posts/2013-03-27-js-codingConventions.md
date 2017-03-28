---
title: JavaScript编码规范
---
前言

此文摘录[w3schools](https://www.w3schools.com/js/js_conventions.asp)

使用相同的编码规范的优点。

* 提高代码的可读性
* 简化代码维护

****
# 编码规范

**一、空格围绕着运算符**

**二、代码缩进**

总是使用4个空格缩进的代码块:

实例

```js
function toCelsius(fahrenheit) {
    return (5 / 9) * (fahrenheit - 32);
}
```

**三、声明规则**

* '{' 放在第一行的末尾
* 在'{'的前面加一个空格
* 以'}'开启新的一行，前面不加空格
* 表达式语句前面加上四个空格，语句以';'结束。
* '}'后面不要加';'

函数：

```js

function toCelsius(fahrenheit) {
    return (5 / 9) * (fahrenheit - 32);
}

```

循环：

```js

for (i = 0; i < 5; i++) {
    x += i;
}

```

条件语句：

```js

if (time < 20) {
    greeting = "Good day";
} else {
    greeting = "Good evening";
}

```

**四、对象的规则**

* '{'同对象的名字在同一行
* 在属性和它的值之间使用冒号+空格
* 属性的值如果是字符串用引号包围，如果是数字则不用。
* 多个属性值之间用','号分隔。
* '}'开启新的一行，前面不要加空格
* 结束后用';'

实例：

```js

var person = {
    firstName: "John",
    lastName: "Doe",
    age: 50,
    eyeColor: "blue"
};

```

**五、line length < 80**

为了可读性,避免行超过80个字符。

如果一个JavaScript语句不适合在一行上,更换下一行,最好的拦截点是操作符或逗号后面。


