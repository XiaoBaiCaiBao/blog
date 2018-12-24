---
title: Javascript Dom 编程艺术（2th edition）笔记
layout: post
categories: ''
tags: ''
---
## 2.1 准备工作

### 三种执行js代码的方式，后面的方式的好处大于前面的

1. 将js代码放到html文档&lt;head&gt;标签中的&lt;script&gt;<br/>标签之间
&lt;script&gt;标签中有type="text/javascript"属性，不写也可，默认即为javascript。
2. 单独一个js文件。在文档&lt;head&gt;标签中&lt;script&gt;标签中的src属性指向该文件。
3. 把&lt;script&gt;标签放在HTML文档最后，&lt;/body&gt;标签之前。

### 解释型和编译型程序设计语言

> Programming languages are either interpreted or compiled. Languages like Java or C++ require a
compiler. A compiler is a program that translates the source code written in a high-level language like
Java into a file that can be executed directly by a computer.

> Interpreted languages don’t require a compiler—they just need an interpreter instead. With
JavaScript, in the context of the World Wide Web, the web browser does the interpreting. The JavaScript
interpreter in the browser executes the code directly from the source. Without the interpreter, the
JavaScript code would never be executed.

> If there are any errors in the code written in a compiled language, those errors will pop up when the
code is compiled. In the case of an interpreted language, errors won’t become apparent until the
interpreter executes the code.

> Although compiled languages tend to be faster and more portable than interpreted languages, they
often have a fairly steep learning curve.

## 2.2 语法

### 语句是否加分号

> You can simply separate statements by placing them on different lines.

> If you place a number of statements on the same line, you must separate them with semicolons.

### 变量声明

1. 每行单独声明  
var age;  
var mood;
2. 一条语句一次声明多个变量  
var mood, age;
3. 声明同时对变量赋值  
var mood = "happy";  
var age = "23";  
或  
var mood = "happy", age = "23";

### 命名

1. 变量及其他语法元素**区分大小写**