## Welcome to Sherry's HTML&CSS study summary

You can use the [HTML](##html学习总结) to see HTMLstudy summary.

You can use the [CSS](#css学习总结) to see CSS study summary.

# HTML
- [HTML学习总结](#html学习总结)
    - [HTML介绍](#html介绍)
      - [定义](#定义)
      - [特点](#特点)
    - [HTML的标签](#html的标签)
      - [基本标签](#基本标签)
        - [HTML标签](#html标签)
        - [head标签](#head标签)
        - [body标签](#body标签)
    - [段落与文字标签](#段落与文字标签)
    - [文本格式化标签](#文本格式化标签)
    - [自闭合标签](#自闭合标签)
      - [一般标签](#一般标签)
      - [自闭合标签](#自闭合标签-1)
    - [超链接和锚点](#超链接和锚点)
      - [超链接](#超链接)
      - [锚点](#锚点)
        - [用途](#用途)
        - [操作](#操作)
    - [图片和文件路径](#图片和文件路径)
      - [图片](#图片)
      - [文件路径](#文件路径)
        - [绝对路径](#绝对路径)
        - [相对路径](#相对路径)
    - [区块元素和内联元素](#区块元素和内联元素)
      - [区块元素](#区块元素)
        - [特点](#特点-1)
        - [常见区块元素](#常见区块元素)
      - [内联元素](#内联元素)
        - [特点](#特点-2)
        - [常见内联元素](#常见内联元素)
      - [内联块元素](#内联块元素)
        - [特点](#特点-3)
        - [常见的内敛块元素有](#常见的内敛块元素有)
    - [pre预设格式标签](#pre预设格式标签)
    - [table标签](#table标签)
    - [列表](#列表)
      - [无序列表](#无序列表)
      - [有序列表](#有序列表)
    - [表单](#表单)

### HTML介绍

#### 定义
HTML是超文本标记语言（HyperText Markup Language）的缩写。HTML 不是一门编程语言，而是一种用于定义内容结构的标记语言。

#### 特点

* 通过标签来定义，代码由标签组成

* 不区分大小写，建议使用小写

* 整段代码 < html>开始 < /html>结束

* 内部=头部分（< head>开始 < /head>结束）加体部分（< body>开始 < /body>结束）

* head部分最先加载

### HTML的标签

#### 基本标签

##### HTML标签

整个网页是从\<html>这里开始的，然后到\</html>结束。

##### head标签

head标签代表页面的“头”，定义一些特殊内容，这些内容往往都是“不可见内容”（在浏览器不可见）。
|\<head>内部标签|解释|
|:-----------------:|:----:|
|\<title>|网页的标题|
|\<meta>|网页的基本信息|
|\<style>|定义CSS样式|
|\<link>|链接外部CSS文件或脚本文件|
|\<script>|脚本语言|
|\<base>|页面所有链接的基础定位|

##### body标签

body标签代表页面的“身”，定义网页展示内容，这些内容往往都是“可见内容”（在浏览器可见）。

### 段落与文字标签

|标签|语义|说明|
|:----:|:----:|:-----:|
|\<h1>~\<h6>|header|标题（1~6标题醒目程度逐级递减）|
|\<p>|	paragraph|段落|
|\<br>|	break|	换行|
|\<hr>|	horizontal rule|水平线|
|\<div>|division|分割（块元素）|
|\<span>|span|区域（行内元素）|

### 文本格式化标签

注：文本格式化建议用CSS，HTML 是用来表现页面内容而不是对页面进行修饰的，专门的页面美化需要使用CSS。
|标签|语义|说明|
|:----:|:------:|:------:|
|\<strong>|strong（加强）|加粗|
|\<em>|emphasized（强调）|斜体|
|\<small>|small（变小）|使文本变为较小号的字体|
|\<u>|underline(下划线)|文本下添加下划线|

### 自闭合标签

HTML标签分为2种，一种是“一般标签”，另外一种是“自闭合标签”。

#### 一般标签

一般标签有开始符号和结束符号，如\<body>\</body>可以在开始符号和结束符号之间插入其他标签或文字。

#### 自闭合标签

自闭合标签只有开始符号没有结束符号，如\<br/>、\<hr/>由于没有结束符号，不能插入其他标签或文字，只能定义自身的属性。

### 超链接和锚点

#### 超链接

    <a href="链接" target="_blank">你想在页面上链接显示的文字</a>

其中，href即为要跳转去的地址 URL（Uniform Resorce Locator)，target属性为_blank表示在新的页面打开超链接（默认是在当前页面打开即_self）

#### 锚点

锚点，也称为书签，用于标记页面的某个元素或位置。

##### 用途

通过锚点，可以轻易的在长页面内实现跳转。

##### 操作

先使用id属性（元素的id值必须是唯一的）生成某元素的锚点，然后再使用超链接指向该锚点（超链接中的地址需要有#符号即可。

    <h2 id="C4">第四章 论零号病人的重要性</h2>
      <a href="#C4">跳到第四章</a>

### 图片和文件路径

#### 图片

    <img src="图片文件位置/链接" alt="获取图片出现问题时显示的文字，占位符作用">

注：可添加width、height属性设定图片大小，但不建议使用，可能导致图片变形。

#### 文件路径

为获取图片文件，我们需要指定该文件位于何处，这称为文件路径。文件路径有相对路径和绝对路径两种。

##### 绝对路径

图片链接，如https://www.yulumi.cn/gl/uploads/allimg/201128/162003D24-2.jpg

##### 相对路径

图片文件相对于当前文档的位置。

其中，.表示当前目录，..表示上一级目录
|例子|说明|
|:-----:|:-----:|
|\<img src="picture.jpg">|该图片文件与当前文档在同一目录中|
|\<img src="./images/picture.jpg">|该图片文件在当前目录下的images目录中|
|\<img src="../picture.jpg">|该图片文件在上一级目录中|

### 区块元素和内联元素

#### 区块元素

区块元素在浏览器显示时，通常会以新行来开始（和结束）。

##### 特点

* 每个元素独占一行，默认情况下宽度等于父元素的宽度。
* 不设置高度时，高度为0，有内容时高度由内容撑开，不解析换行符。
* 可以设置width、height、margin、padding属性。
* dispaly:block。

##### 常见区块元素

* div（盒子）、 address（ 定义地址）
* ul（无序列表）、ol（有序列表）、li（列表的项）
* dl（定义列表）、dd（定义列表中定义条目）、dt（定义列表中的项目）
* p（段落）、h1~h6（网页中的标题，从大到小）
* table（表格）、td（标准单元格)、tr（行）、th(表头单元格)
* form（表单）、pre（预格式化文本）、hr（分割线）
* caption （表格标题）、thead(表格表头)、tbody（表格主体）

#### 内联元素

内联元素，总是一个接一个进行显示，不会新起一行。

##### 特点

* 相邻的元素会排列在同一行，排不下时会自动换行
* 不支持宽高属性，宽高完全由内容撑开，会解析换行符
* 使用部分样式会出错（上下margin和padding等）,只能设置margin-left、margin-right、padding-left、padding-right.(可以出现效果)
* dispaly:inline

##### 常见内联元素

* span（行间元素） 、textarea（多行文本输入控件）
* b（加粗）、strong（加重）、i（斜体）、em（着重）
* sub（下标）、sup（上标）
* ins（插入）、del（删除）、br（换行）、a（定义锚以及超链接）
* img（图片）、input（表单项）、label（表单标记）
* big（大号字体加粗）、small9(呈现小号字体效果）
* code（定义计算机代码文本）、q（定义短的引用）、select（定义单选或者多

注：虽然input和img都是行内元素，但是它们是可以设置宽和高的。主要是因为它们是内敛块元素。

#### 内联块元素

内联块状元素（inline-block）就是同时具备内联元素、块状元素的特点

##### 特点

* 和其他元素都在一行上；

* 元素的高度、宽度、行高以及顶和底边距都可设置。

##### 常见的内敛块元素有

* img(图片)

* input（表单项）

* iframe（框架）

* canvas（画布）

* video（视频）

* audio（音频）

### pre预设格式标签

\<pre>标签使文本以一定的格式展示

注：在 HTML 中，某些字符是预留的。在 HTML 中不能使用小于号（<）和大于号（>），这是因为浏览器会误认为它们是标签。
如果希望正确地显示预留字符，必须在 HTML 源代码中使用字符实体（character entities）

### table标签

\<table>\</table>标签使页面的内容用表格来进行呈现,其中，\<tr>表示行, \<td>表示行中的单元,\<th>是表头的单元（将会加粗显示）

    <table>
     <tr>
      <th>1\</th>
     </tr>
     <tr>
      <td>MAX\</td>
     </tr>
    </table>

### 列表 

#### 无序列表

无序列表使用\<ul>标签，默认使用实心圆点作为每项的标志，其它的标志可以是空心圆circle，实心方块square以及不出现标志。

#### 有序列表

有序列表使用\<ol>标签，默认使用数字作为每项的标志，其它的标志可以是大写字母A，小写字母a，罗马字母i等。

### 表单

使用\<form>\</form>标签。




# CSS学习总结

- [CSS学习总结](#css学习总结)
    - [CSS介绍](#css介绍)
      - [什么是CSS](#什么是css)
      - [CSS作用](#css作用)
      - [基本用法](#基本用法)
    - [CSS应用方式](#css应用方式)
      - [外部样式表](#外部样式表)
      - [内部样式表](#内部样式表)
      - [内联样式](#内联样式)
    - [选择器](#选择器)
      - [标签选择器](#标签选择器)
      - [类选择器](#类选择器)
      - [ID选择器](#id选择器)
      - [组合选择器](#组合选择器)
      - [子选择器](#子选择器)
      - [伪类选择器](#伪类选择器)
      - [伪元素选择器](#伪元素选择器)
      - [选择器优先级](#选择器优先级)
    - [盒子模型](#盒子模型)
    - [边框和边距设置](#边框和边距设置)

### CSS介绍

#### 什么是CSS

CSS是级联样式表（Cascading Style Sheets）的缩写。简单来说，是一组样式设置的规则，用于控制页面的外观样式。

HTML 用于撰写页面的内容，而 CSS 将决定这些内容该如何在屏幕上呈现。

#### CSS作用

页面外观美化
布局和定位

#### 基本用法

 CSS语法

![css语法图片](../image/css语法.png)

选择器：要修饰的对象（东西）
属性名：修饰对象的哪一个属性（样式）
属性值：样式的取值

例：

    p{
        color:red;
        text-align:center;
     }

### CSS应用方式

三种应用方式：外部样式表，内部样式表，内联样式

#### 外部样式表

使用单独的 .CSS 文件定义，然后在页面中使用 link标签 或 @import指令引入

link标签引入
语法：

       <link rel="stylesheet" type="text/css" href="css样式文件的路径">
例：

    <!DOCTYPE html>
     <html>
      <head>
         <meta charset="utf-8">
    <!-- 注意下面这个语句，将导入外部的 mycss.css 样式表文件 -->
        <link rel="stylesheet" type="text/css" href="mycss.css">
        <title>页面标题</title>
      </head>
      <body>
      </body>
     </html>

在需要引入css样式的HTML文件的head部分加入link标签。

@import指令 导入外部样式文件

语法：

    <style>
	  @import "CSS样式文件路径";
	  @import url(CSS样式文件路径);
    </style>

例：

    <!DOCTYPE html>
    <html lang="en">
    <head>
	  <meta charset="UTF-8">
	  <title>Document</title>
	<!-- import导入外部样式文件 -->
	  <style>
		/* @import "style/hello.css" */
		@import url(style/hello.css);
	  </style>
    </head>

#### 内部样式表

内部样式表直接使用\<style> \</style>标签将样式放在HTML文件中。

例:


    <!DOCTYPE html>
     <html>
      <head>
         <meta charset="utf-8">
        <style>
        body {
          background-color: linen;
          text-align: center;
        }
        h1 {
           color: red;
        }
         .haha {
            margin-top: 100px;
            color: chocolate;
            font-size: 50px;
        }
        </style>
      </head>
      <body>
      </body>
     </html>

#### 内联样式

内联样式就是直接把样式规则直接写到要应用的元素中。

例：

    <h3 style="color:green;">I am a heading</h3>

三种样式中，引入外部样式表是使用样式的主流方式，因为众多的样式规则单独放在一个文件中，与 HTML 内容分开，结构清晰。同时其它页面也可使用，达到复用的目的。

内部样式表适用于页面样式规则较少时。

内联样式是最不灵活的一种方式，完全将内容和样式合在一起，实际应用中非常少见。

级联的优先级

哪个样式定义离元素的距离近，哪个就生效。

从高到低：内联样式->内部样式表或外部样式表->浏览器缺省样式

### 选择器

#### 标签选择器

也称为元素选择器，使用HTML标签作为选择器的名称

以标签名作为样式应用的依据

例：
样式规则

        p{
			color:red;
			font-size:20px;
		}

使用

    <p>welcome to css!</p>

#### 类选择器

使用自定义的名称，以 . 号作为前缀，然后再通过HTML标签的class属性调用类选择器。
以标签的class属性作为样式应用的依据。

例：

样式规则

    .center{
    text-align: center;
    }
使用

    <p class="center">我会居中显示的</p>

#### ID选择器

使用自定义名称，以 # 作为前缀，然后通过HTML标签的id属性进行名称匹配。

以标签的id属性作为样式应用的依据，一对一的关系。

例：

样式规则

    #sky{
    color: blue;
    }
使用

    <p id="sky">蓝色的天空</p>

#### 组合选择器

也称为集体声明，将多个具有相同样式的选择器放在一起声明。

后代选择器

以空格作为分隔，如：.haha p 代表在div元素内有.haha这种类的所有元素。

例：

     <html>
     <head>
       <style>
        .haha p {
        background-color: yellow;
        }
       </style>
     </head>
     <body>
       <div class="haha">
       <p>Paragraph 1 in the div .haha.</p>
       </div>
       <p>Paragraph 4. Not in a div .haha.</p>
     </body>
     </html>

#### 子选择器

也称为直接后代选择器，以>作为分隔，如：.haha > p 代表在有.haha类的元素内的直接<p>元素。

例：

    <html>
    <head>
      <style>
        .haha > p {
        background-color: yellow;
        }
      </style>
    </head>
    <body>
      <div class="haha">
      <p>Paragraph 1 in the div .haha.</p>
      <p>Paragraph 2 in the div .haha.</p>
      <span>
        <p>Paragraph 3 in the div .haha - it is descendant but not immediate child.</p>
       </span> <!-- not Child but Descendant -->
      </div>
      <p>Paragraph 4. Not in a div .haha.</p>
     <p>Paragraph 5. Not in a div .haha.</p>
    </body>
    </html>

虽然段落3在.haha类中，但它的直接父元素是span，不是.haha的直接后代，所以不能选择。只有段落1、2有黄色背景。

#### 伪类选择器

根据不同的状态显示不同的样式，一般多用于 标签

使用方法：需要修饰的标签：伪类{样式定义}

四种状态：

:link 未访问的链接
:visited 已访问的链接
:hover 鼠标悬浮到连接上，即移动在连接上
:active 选定的链接，被激活

#### 伪元素选择器

使用方法：需要修饰的标签：伪元素{样式定义}

:first-letter 为第一个字符的样式
:first-line 为第一行添加样式
:before 在元素内容的最前面添加的内容，需要配合content属性使用
:after 在元素内容的最后面添加的内容，需要配合content属性使用

#### 选择器优先级

行内样式>ID选择器>类选择器>标签选择器

原因：首先加载标签选择器,再加载类选择器，然后加载ID选择器，最后加载行内样式后加载会覆盖先加载的同名样式

可以使用!important使某个样式有最高的优先级

### 盒子模型

所有HTML元素可以看作盒子，在CSS中，"box model"这一术语是用来设计和布局时使用。

CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：边距，边框，填充，和实际内容。

盒模型允许我们在其它元素和周围元素边框之间的空间放置元素。

从内到外，这个盒子是由内容 content, 内边距 padding, 边框 border, 外边距 margin构成的.

![盒子模型图片](../image/盒子模型.png)

Margin(外边距) - 清除边框外的区域，外边距是透明的。
Border(边框) - 围绕在内边距和内容外的边框。
Padding(内边距) - 清除内容周围的区域，内边距是透明的。
Content(内容) - 盒子的内容，显示文本和图像。

一个元素真正占据的宽度应该是：
左外边距 + 左边框宽度 + 左内边距 + 内容宽度 + 右内边距 + 右边框宽度 + 右外边距

### 边框和边距设置

无论边框、内边距还是外边距，它们都有上下左右四个方向。默认顺序为上，右，下，左，或记为顺时针方向。

例：

    padding: 20px; /* 上下左右都相同 */
    padding-top: 20px;
    padding-bottom: 100px;
    padding-right: 50px;
    padding-left: 80px;
    padding: 25px 50px 75px 100px; /* 简写形式，按上，右，下，左顺序设置 */
    padding: 25px 10px; /* 简写形式，上下为25px，左右为10px */
