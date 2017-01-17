###JS发展历史

Netscape: navigator

* 1995    JavaScript--像极了Java，但比java简单
  ```
  Java "write once run anywhere"
  ```
* 1996    JavaScript 1.1 --&gt; ECMA

* ECMAScirpt标准--&gt;定义了js语言的核心语法

* Netscape--&gt;遵照标准，实现了JavaScript语言

* Microsoft--&gt;遵照标注，实现了JScript语言

W3C: DOM标准--&gt;专门操作网页内容的标准  
     **所有浏览器都兼容的标准**

BOM: 专门操作浏览器窗口的编程接口

`js = ECMAScript + DOM + BOM`

浏览器两大引擎：  
     1. 内容排版引擎 ---解析HTML/CSS  
     2. 脚本解释引擎 ---解析Javascript

---

### 声明提前

***在程序正式执行前，都会将所有var声明的变量提前到开始位置，集中创建。但是赋值留在原地！***

```javascript
console.log(b)     //抛出异常
b = 10 ;
console.log(b)
//Uncaught ReferenceError: b is not defined(anonymous function) 
```
对比
```javascript
console.log(b)     //undefined
var b = 10 ;
console.log(b)
```
可以看出，就多了一个var声明。由于var声明的被提前，所以第二个block中的b只是undefined，而第一个block就直接出错！

* ReferenceError：未声明的变量直接使用。就会出错！
* 没用var声明，但是进行了赋值的，会自动帮你声明，不会出错。但不会声明提前！

     ```javascript
     a = 10 ;
     console.log(a)       //输出： 10
     ```
---
###数据类型
js中有两大数据类型：
* 原始类型:值保存在变量本地的数据类型。有5种：
     * Number：  保存数字的类型
     * String:   保存字符串的类型
     * Boolean:  保存真、假二选一的类型
     * undefined 只有一个值undefined
     * null      表示不指向任何地址
* 引用类型


