---
title: Javascript Dom 编程艺术（2th edition）笔记
layout: post
categories: ''
tags: ''
---
## 2.1 准备工作

#### 三种执行js代码的方式，后面的方式的好处大于前面的

1. 将js代码放到html文档&lt;head&gt;标签中的&lt;script&gt;<br/>标签之间
&lt;script&gt;标签中有type="text/javascript"属性，不写也可，默认即为javascript。
2. 单独一个js文件。在文档&lt;head&gt;标签中&lt;script&gt;标签中的src属性指向该文件。
3. 把&lt;script&gt;标签放在HTML文档最后，&lt;/body&gt;标签之前。

#### 解释型和编译型程序设计语言

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

#### 语句是否加分号

> You can simply separate statements by placing them on different lines.

> If you place a number of statements on the same line, you must separate them with semicolons.

#### 变量声明

js允许直接对变量赋值，而无需事先声明。

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

#### 命名

1. 变量及其他语法元素**区分大小写**
2. 变量名允许包含字母、数字（但第一个字符不允许是数字）、美元符号和下划线
3. 驼峰命名是函数名、方法名和对象属性名命名的首选格式。

#### 数据类型

1. Strings
  * 字符串包裹在单引号双引号里均可
  * 如果字符串里包含引号，并且该引号与包裹着字符串的引号相同，那么必须用反斜线\来转义该引号
2. Numbers
  * js允许任意位小数，这样的数称为浮点数(floating-point numbers)
3. Boolean values
4. Arrays
  * ## 2.1 准备工作

#### 三种执行js代码的方式，后面的方式的好处大于前面的

1. 将js代码放到html文档&lt;head&gt;标签中的&lt;script&gt;<br/>标签之间
&lt;script&gt;标签中有type="text/javascript"属性，不写也可，默认即为javascript。
2. 单独一个js文件。在文档&lt;head&gt;标签中&lt;script&gt;标签中的src属性指向该文件。
3. 把&lt;script&gt;标签放在HTML文档最后，&lt;/body&gt;标签之前。

#### 解释型和编译型程序设计语言

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

#### 语句是否加分号

> You can simply separate statements by placing them on different lines.

> If you place a number of statements on the same line, you must separate them with semicolons.

#### 变量声明

js允许直接对变量赋值，而无需事先声明。

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

#### 命名

1. 变量及其他语法元素**区分大小写**
2. 变量名允许包含字母、数字（但第一个字符不允许是数字）、美元符号和下划线
3. 驼峰命名是函数名、方法名和对象属性名命名的首选格式。

#### 数据类型

1. Strings
  * 字符串包裹在单引号双引号里均可
  * 如果字符串里包含引号，并且该引号与包裹着字符串的引号相同，那么必须用反斜线\来转义该引号
2. Numbers
  * js允许任意位小数，这样的数称为浮点数(floating-point numbers)
3. Boolean values
4. Arrays
  * 字符串、数值和布尔值都是标量，标量只能有一个值。如果变量用来存储一组值，就要用数组。
  * 声明数组用Array关键字
    * 声明同时指定数组初始元素个数，即数组的长度  
    var beatles = Array(4)
    * 也可不给出元素个数  
    var bealtles = Array()
    * 在声明同时填充数组  
    var beatles = Array("0", "1", "2", "3")  
    或者直接方括号括起来  
    var beatles = ["0", "1", "2", "3"]
  * 数组元素可以是字符串，布尔值，数值。并且数组每一项元素类型可以不同，混合在一起。
  * 数组元素还可以是变量
    * var name = "John";
    * beatles [0] = name;
  * 数组元素的值还可以是另一个数组的元素；还可以包含其他的数组，用beatles[0][0]获取
  * 关联数组,不推荐使用
5. Objects

#### 操作

* "=="用于比较，"==="严格比较，不仅比较值，而且会比较变量的类型。  
false == "" 结果为true。因为相等操作符==认为空字符串与false的含义相同。
* 逻辑操作符 "&&" "||" "!"

#### 循环

* while
* do while
* for

#### 作用域
      function square(num){
        total = num * num;
        return total;
      }
      var total = 50;
      var number = square(20);
      alert(total);
  * 结果弹出400。
  * 在函数内部用var关键字声明变量，该变量是局部变量。否则是全局变量，会影响全局。代码应改为：
        function square(num) {
          var total = num * num;
          return total;
        }
  * 函数在行为方面应该像一个自给自足的脚本，在定义函数时，要把它内部的变量全都明确地声明为局部变量。在函数里使用var关键字来定义变量，就能避免任何形式的二义性隐患。

#### 对象 第二章最后一节

* 包含在对象里的数据可以通过两种形式访问——属性(property)和方法(method)。
* 属性是隶属于某个特定对象的变量；方法是只有某个特定对象才能调用的函数。
* 对象就是有一些属性和方法组合在一起而构成的一个数据实体。
* 实例是对象的具体个体。创建新实例用new关键字：var jeremy = new Person;**要不要加括号？**。**望搞清楚！**
* **内建对象** 和 **宿主对象** **望再读！**

## 第3章 DOM

* 与某个特定对象相关联的变量被称为这个对象的属性，只能通过某个特定对象去调用的函数被称为这个对象的方法。
* js对象可分为三种类型
  1. 用户定义对象(user-defined object)：由程序员自行创建的对象。
  2. 内建对象(native object)：内建在js语言里的对象，如Array,Math和Date等。
  3. 宿主对象(host object)：由浏览器提供的对象。如window对象。
    * window对象对应着浏览器窗口本身，这个对象的属性和方法通常统称为BOM(浏览器对象模型)。提供了window.open和window.blur等对象。

#### 获取元素的三种方法

* 获取id属性值是purchases的元素包含着多少个列表项：
        var shopping = document.getElementById("purchases");
        var items = shopping.getElementsByTagName("*");

* `document.getElementsByClassName("important sale").length;`表示同时带有"important"和"sale"类名的元素

#### 获取和设置属性

* `object.getAttribute(attribute)`
* 如果getAttribute没有值，会返回null,它的含义是“没有值”。if(sth)和if(sth != null)完全等价
* `object.setAttribute(attribute, value)`

## 第4章

#### setAttribute修改属性和直接打点修改属性(4.2.1 非DOM解决方案)

* **DOM Level 1？？？**
* return false 和 preventdefault？

#### Dom的其它属性

* elements.childNodes。返回的数组包含所有类型的节点，而不仅仅是元素节点，比如空格和换行符都会被解释为节点。
* node.nodeType的值有3种有实用价值
  * 元素节点的nodeType = 1
  * 属性节点的nodeType = 2
  * 文本节点的nodeType = 3
* node.nodeValue。改变文本节点的值，可用来得到和设置一个节点的值。
  * img dom2
* `node.firstChild` 等价于 `node.childNodes[0]`
* `node.lastChild` 等价于 `node.childNodes[node.childNodes.length - 1]`

## 第5章

#### 平稳退化
* window.open(url, name, features)
  * 第一个参数
  * 第er个参数
  * 第san个参数
* "javascript:"伪协议。`<a href="javascript:popUp('http://www.example.com/');">Example</a>` 这种做法非常不好。
  * 在支持伪协议的浏览器中运行正常。
  * 较老的浏览器会尝试打开那个连接失败。
  * 支持伪协议但禁用了javascript功能的浏览器会什么也不做。
* 内嵌的事件处理函数。`<a href="#" onclick="popUp('http://www.example.com/')"; return false;>Example</a>`。这种做法也不能平稳退化。
* `<a href="http://www.example.com/" onclick="popUp('http://www.example.com/')"; return false;>Example</a>`。这是一个平稳退化的例子。

## 第6章

* 平稳退化
* js与HTML是分离的。不让js代码对这个网址的结构有任何依赖。
  `if(!...) return false`
* 匿名函数      
      dom.onclick = function(){
        fun(this);
      }
* onclick事件的所有功能赋给onkeypress事件。但不要使用onkeypress处理函数。P90
  `dom.onkeypress = dom.onclick;`

## 第7章