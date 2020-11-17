## 1.HTML/CSS/JavaScript学习（2020.11.07）

### 1.visual studio的安装

今天打算学习JavaScript的时候更新visual studio，安装java组件时遇到visual studio installer卡在提取文件不动的情况。经过百度得到解决方案。校园网是真的慢....Node.js组件就给我下了好久。。

1. 更改DNS：将其设置为114.114.114.114或8.8.8.8
2. 目前还未知DNS的一些知识，学习之后回来补充。

![image test](C:\Users\windows\Desktop\计算机作业\geek考核\Visual studio.png)

### 2.visual studio code的安装

## 2.浏览器及其内核 ##

### 1. 常用的浏览器

 IE浏览器，现在也称Edge浏览器，火狐浏览器(firefox)，谷歌浏览器(chrome)，苹果浏览器(Safari)

### 2. 浏览器的内核

渲染引擎和JS引擎

渲染引擎负责取得网页的内容（HTML、XML、图像等）、整理讯息（加入css）、计算网页的显示方式，然后输出到显示器给用户直观的感受。

JS引擎则是解析Javascript语言，执行javascript语言来实现网页的动态效果。

以上则成为我们所说的前端。前端即网站前台部分，运行在PC端，移动端等浏览器上展现给用户浏览的网页。

而前端开发则是网站的前台代码实现，包括基本的HTML和CSS一级JavaScript。

而对于HTML CSS JavaScript三者的关系可以用下面这个图表示。

```mermaid
%% 语法示例
        gantt
        dateFormat  YYYY-MM-DD
        title 三者关系图
        section 三者关系
        ..                      :done,    des1, 
        CSS（把网页做得更加美观）                      :active,  des2, after des1,5d
              JavaScript（编程语言，用来控制 HTML）                     : des3, after des2, 5d
        HTML （网页核心，实现web页面的显示）                     :done,    des4, after des3, 5d
 
```

### 3.JavaScript/HTML/CSS的关系

html是主体，装载各种dom元素；css用来装饰dom元素；javascript控制dom元素。
用一扇门比喻三者间的关系是：html是门的门板，css是门上的油漆或花纹，javascript是门的开关。

1. **HTML** 定义了网页的内容
2. **CSS** 描述了网页的布局
3. **JavaScript** 网页的行为

---



## 3.初识html ##

### 3.1对html的认识。 ###

html（全称HyperText Markup Language)是一种用于创建网页的标准标记语言。

web站点，我们俗称的网站是由html建立的，运行在浏览器上，由浏览器来解析。这也是为什么无论是电脑，手机，平板想要浏览网页，首先都需要下载浏览器的原因。今天正式学习一下关于网页中html的知识。

### 3.2html代码分析 ###

首先从菜鸟教程上载一个简单的html代码进行分析

```c
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
</head>
<body>
 
<h1>我的第一个标题</h1>
 
<p>我的第一个段落。</p>
 
</body>
</html>
```

​         **代码第一行**`<! doctype html>`.声明html文档的类型用来告诉浏览器页面的文档类型，用来制定html版本的规范。有点类似c语言中开头的`int main( )`

---

​        **代码第二行**`<html lang="en">` 向搜索引擎表示该页面是html语言，并且语言为英文网站，`lang`的意思就是`language`，语言的意思，而`en`则表示为`english`。如果想将页面修改为中文，可以改为`<html lang="zh">`    

---

​       **代码第三行**< head > head元素规定了文档相关的配置信息，文档（页面）的标题，引用的文档样式和脚本等。下面列出一些head标签中放的元素。

1. `title` 网页的标题。`title`将会被显示在浏览器的标题栏，，或用户收藏夹等醒目位置。
2. `link`规定了外部资源与当前文档的关系。
3. `style`包含文档的样式信息或者文档的部分内容。默认情况下，该标签的样式信息为CSS。
4. `base`指定用于一个文档中包含的所有相对URL的根URL。一份中只能有一个<base>元素。
5. `meta`表示那些不能由其他html元相关元素(`base`  `link` `script` `style` `title`)之一表示的任何元数据信息。name 属性和 http-equiv 属性，charset属性。
6. `script`用于嵌入或引用可执行脚本。

==name属性==主要用于描述网页，对应属性为**content**，以便于搜索引擎机器人查找、分类。

<meta name="keywords" content="程序员,程序猿,攻城狮"/>

==http-equiv==类似于HTTP的头部协议，它回应给浏览器一些有用的信息，以帮助正确和精确地显示网页内容。对应属性为**content**，**content**中的内容为各个参数的变量值。

<meta http-equiv="参数"  content="参数值"/>

==charset==规定HTML文档的字符编码。

---

​          **代码第四行** <meta charset="utf-8">表示该网页为utf-8编码方式。

---

​          **代码第七行**<body>元素定义了HTML文档的主体。

### 3.3一些常用代码

 1.html标题(heading)通过<h1>-<h6>标签定义，按数字从大到小排序

```html
<h1>第一级标题。</h1>
<h2>第二级标题。</h2>
<h3>第三级标题。</h3>
```

         2. html水平线 <hr>用于分割内容。
         3. html注释<!--这是一个注释 -->
         4. 元素<pre>定义预格式文本
         5. 段落<p> 
         6. 换行标签<br>
         7. ​    <div>一般用于页面的布局划分，块级标签。

8.  html超链接<a>  

```html
<a href="url">链接文本</a>
```

9. html   <meta>  标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。

   META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。

   元数据可以使用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他Web服务。

10. `CSS` (Cascading Style Sheets) 用于渲染HTML元素标签的样式。之后还要重点学。

### 3.4  块级元素和内联元素

1. 块级元素（block level element）和内联元素（inline element）的区别

| 块级元素                                        | 行内元素                                                     |
| ----------------------------------------------- | ------------------------------------------------------------ |
| 独占一行,默认情况下，其宽度自动填满其父元素宽度 | 相邻的行内元素会排列在同一行里，直到一行排不下，才会换行，其宽度随元素的内容而变化 |
| 可以设置width，height属性                       | 行内元素设置width，height属性无效                            |
| 可以设置margin和padding属性                     | 行内元素起边距作用的只有margin-left、margin-right、padding-left、padding-right，其它属性不会起边距效果。 |
| 对应于display:block                             | 对应于display:inline；                                       |

2. demo

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        #div1{
      
            background-color: red;      
            border: 1px solid black;
            display: inline;
            margin: 100px;//内联元素只有左右外边距有效
            width: 100px;//内联元素宽高是有内容决定的
            height: 100px;//内联元素宽高是有内容决定的，line-height也可以设置高度
        }
        #div2{
            width: 100px;
            height: 100px;
            background-color: green;
            margin: 100px;
        }
     </style>
</head>
<body>
    <div class="box">hello world</div>
    <div id="div1">内联元素</div>
    <div id="div2">块级元素</div>
</body>
</html>

9-17行为内联元素
18-23行为块级元素
```

---



## 4.初识CSS

### 4.1为什么要学CSS（CSS是什么）

1. 首先什么是CSS（Cascading Style Sheets)层叠样式表，样式通常存储在样式表中，外部样式表可以极大提高工作效率

   Q：怎么提高的？

   A：CSS能够对网页中元素位置的排版进行像素级精确控制，支持几乎所有的字体字号样式，拥有对网页对象和模型样式的编辑的能力。

2. CSS的作用：CSS为HTML提供了一种样式描述，定义了其中元素的显示方式，这也让Web设计增添了更多的可能性。

3. CSS的语言特点：（1）拥有丰富的样式，CSS能够给你的wed提供丰富的文档样式外观，以及设置文本和背景属性的能力；可以给元素创建边框，随意改变文本的大小写方式、修饰方式以及其他页面效果。（2）CSS可以将所有的样式声明同一存放，进行同一管理。可以将相同样式进行归类，也可以将一个CSS样式指定到某个页面元素中，修改时只需要在样式列表快捷搜索到相应的样式声明进行修改即可。（有点类似于C语言中的函数调用，分而治之的思想）

   （3）我认为CSS的最大优点！！页面压缩，当你的web中加入了大量的表格和font元素形成各种规格的文字样式，而将这些放入CSS样式表中，可以有效减少页面的体积，这意味着什么？意味着用户在加载页面是使用的时间也会大大减少。（APPLE官网)

4. CSS的工作原理：CSS类似于物流公司打包快递，将冗杂的仓库，分类包装，按需调用。CSS样式可以直接存储于HTML网页或者单独的样式文件。当外部使用时，样式被装在一个带有文件扩展名.css的“包裹”当中，HTML网页再调取相应的包裹。

   

### 4.2让你的web更美观(CSS的使用方法)

1. CSS是为了更好的渲染HTML元素而引入的。CSS修饰标签的样式，有 "内联" 和 "外引" 两种方式。

   对于大部分标签，以上两种方法均可，且修改父级标签，子级标签特性也会改变。但某些标签确无法通过修改父级标签来改变子级标签特性，如a标签，修改其颜色特性，必须直接修改 a 标签的特性才可。

2. 可以通过以下方式添加到HTML中

   ```java
   内联样式-在HTML元素中使用"style"属性
   内部样式表-在HTML文档头部<head>区域使用<style>元素来包含CSS
   外部引用-使用外部CSS文件
   ```

3. 背景颜色的设置

```java
<body style="background-color:yellow;">
<h2 style="background-color:red;">将该标题的背景颜色设置为红色</h2>
<p style="background-color:green;">将该段落的背景颜色设置为绿色</p>
```

3. 字体的颜色和大小

font-family（字体)，color(颜色),font-size(字体大小)属性来定义文本样式。

```html
<h1 style="font-family:verdana;">标题</h1>
<p style="font-family:arial;color:red;font-size:20px;">  段落  </p>

font-size:字体大小 
属性取值：xx-small(最小)   small(小)     large(大)
        x-small(较小)    medium(正常)   x-large(较大)

font-weight:字体粗细
属性取值：单词[normal正常、bold加粗]； 数字[100-500正常、600-900加粗]）

font-style：字体样式
属性取值：normal(正常)、italic(斜体)
字体颜色:color
```

4. 文本对齐方式

文本的对齐可以对比word，有水平对齐与垂直对齐方式。实例

```html
<h1 style="test-align:center;">居中对齐的标题</h1>

```

5. 内部样式表

当单个文件需要特别样式时，就可以使用内部样式表。你可以在<head> 部分通过 <style>标签定义内部样式表:

```
<head>
<style type="text/css">
body {background-color:yellow;}
p {color:blue;}
</style>
</head>
```

6. 外部样式表

当样式需要被应用到很多页面的时候，外部样式表将是理想的选择。使用外部样式表，你就可以通过更改一个文件来改变整个站点的外观。

```
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

### 4.3  CSS的选择器

1. 选择器是什么？

在CSS中，选择器是一种工具，可以用于快速选择需要添加的元素，对HTML页面中的标签实现一对一，一对多的控制，可以让你的HTML的设计效率提高。选择器由样式的不同又分为6种不同的选择器。

2. 6种不同的选择器。

（1）基础选择器（2）层次选择器（3）伪类选择器（4）伪元素选择器（5）属性选择器（6）标签选择器

### 4.4  CSS的盒子模型



![image test](C:\Users\windows\Desktop\计算机作业\geek考核\CSS盒子模型.png)



---

## 5.JavaScript学习

### 5.1  什么是JavaScript

JavaScript是web的编程语言，所有现代的HTML页面都是用JavaScript

JavaScript是可插入HTML页面的编程代码。

JavaScript插入HTML页面后，可由所有的现代浏览器执行。

### 5.2  JavaScript的用法

1. HTML 中的脚本必须位于 <script> </script> 标签之间。

   脚本可被放置在 HTML 页面的 <body> 和 <head> 部分中。

   这就意味着你想要在HTML页面中插入JavaScript代码就得使用`script`标签，这个标签会告诉JavaScript的起止位置。

2. 语法：数字(number)，字符串(string)，数组(array)，对象(object)，定义变量(var x)，算数运算符，赋值运算符，注释，数据类型。这些都可以和C语言进行类比，其实两者都差不多的。

### 5.3 JavaScript的数据类型

1. 和C语言类似的JavaScript有多种数据类型：number（整数和小数），string（字符串类型），boolean（布尔类型,true or false)，null（空类型)，undefined（未定义)，object(对象)

例如：var length=16(定义一个数组对象，他表示数组的长度)

​            var carname="Volvo XC60"(定义一个字符串对象)

​            var x1=34.00(定义数字，小数点可以带也可以不带)

---

注意：JavaScript对字母的大小写十分敏感！

​           JavaScript语法下`16+"Volvo"`的输出结果为==16Volvo==和C语言有所区别（数据类型的知识）

​           JavaScript 中，常见的是驼峰法的命名规则，如 lastName (而不是lastname)。 

---

### 5.4 JavaScript的数组

1. 数组的定义方式和C语言的类似，数组下标都是基于零，第一个项目是[0]。因此其定义方式也和C语言类似。

```javascript
var cars=number[1,2,3,4,5]

数组的输出
<!DOCTYPE html>
<html>
<body>

<script>
var num = new Array(1,2,3,5,6);
for(var i=0;i<5;i++){
    document.write(num[i] + "<br>");
}
</script>
</body>
</html>
```

### 5.5 JavaScript的变量

1. 声明变量(给变量取名称方便与查看和调用)

```javascript
var carname=new String;
var x=      new Number;
var y=      new Boolean;
var cars=   new Array;
var person= new Object;
```

### 5.6 JavaScript的对象

1. 在JavaScript中的所有事物都是对象：如字符串、数组、数值，此外JavaScript允许自定义变量，并且提供多个内建对象。

2. 访问对象的属性（对象名称.属性。如x=message.length 长度）

3. 访问对象的方法（调用）

4. 创建JavaScript对象

   通过 JavaScript，定义并创建自己的对象。

   创建新对象有两种不同的方法：使用 Object 定义并创建对象的实例。使用函数来定义对象，然后创建新的对象实例。

