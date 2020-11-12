---
cover: 'https://source.unsplash.com/user/erondu/1440x960'
coverWidth: 1200
coverHeight: 750
title:
categories: JavaScript
tags: ES6
top:
permalink:
---
<!--more-->



## ES6

#### ES6是什么

es6是ECMA为JavaScript订制的第6个版本,2015年6月发行,涵盖了2015 - 2020

#### ES6特性

- 表达式
  - [声明 (let/const)](#### 声明)
  - 解构赋值
- 内置对象
  - 字符串扩展
  - 数值扩展
  - 对象扩展
  - 数组扩展
  - 函数扩展
  - 正则扩展
  - Symbol / set /Map / Proxy /Reflect
- 语句与运算
  - class
  - Module
  - Iterator
- 异步编程
  - Promise
  - Generator
  - Async



#### 声明

- let (声明变量,类似var,但是只在代码块中有效)
  - let声明的变量只在所处于的块级有效；
  -  let没有‘变量提升’的特性，而是‘暂时性死区（temporal dead zone）’特性
- const (声明常量)
  - 声明恒定变量，声明的同时就必须赋值，否则会报错

#### 块级作用域:

##### ES6之前

- 全局作用域
- 函数作用域

因此会产生变量提升的问题

```
function func(){
    console.log(test);
    var test = 1;
};
func();
//undefind
在进入func之前,所有通过var声明的变量提前声明并赋予undefinded值
```

##### ES6

- 全局作用域
- 函数作用域
- 块级作用域

```
function f1() {
  let n = 5;
  if (true) {
    let n = 10;
  }
  console.log(n); // 5
}


function f1() {
  var n = 5;
  if (true) {
    var n = 10;
  }
  console.log(n); // 10
}
```

