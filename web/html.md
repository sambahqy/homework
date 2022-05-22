# HTML
## 一.html的定义
HTML是**超文本标记语言**，是一种定义内容结构的标记语言，定义了**网页的含义和结构**  
 
 ---
## 二.html文档结构分析

### 1.对一个html元素的简单剖析（以`<p></p>`为例）
 开始标签（Opening tag）：包含元素的名称，被左、右角括号所包围。表示元素从这里开始或者开始起作用 —— 在本例中即段落由此开始。<br>
 结束标签（Closing tag）：与开始标签相似，只是其在元素名之前包含了一个斜杠。这表示着元素的结尾 —— 在本例中即段落在此结束。初学者常常会犯忘记包含结束标签的错误，这可能会产生一些奇怪的结果。<br>
 内容（Content）：元素的内容，本例中就是所输入的文本本身。<br>
 元素（Element）：开始标签、结束标签与内容相结合，便是一个完整的元素。<br>
 ### 2.分析 HTML 文档
 对于我们创建的 HTML 文档，前面生成的框架进行如下分析：

`<!DOCTYPE html>`: 声明文档类型。

`<html></html>`: 这个元素包裹了整个完整的页面，是一个**根元素**，其它元素都嵌套到其中。

`<head></head>`: 这个元素是一个容器，它包含了所有你想包含在HTML页面中但不想在HTML页面中显示的内容。这些内容包括你想在搜索结果中出现的关键字和页面描述，CSS样式，字符集声明等等。

`<meta charset="utf-8">`: 这个元素设置文档使用utf-8字符集编码.

`<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">`: 指定页面的图标，出现在浏览器标签上。

`<title></title>`: 设置页面标题，出现在浏览器标签上.

`<body></body>`: 包含你能在页面看到的所有内容，包括文本，图片，音频，游戏等等。
---
### 三.HTML元素
#### 1.HTML标题
标题是通过`<h1>`-`<h6>`标签定义的
如
  ````
  <h1>这是一个标题。</h1>
  <h2>这是一个标题。</h2>
  <h3>这是一个标题。</h3>
  ````
  $\color{red}{注：}$会自动给标题换行  
  ***
  #### 2.HTML段落
  HTML可以将文档分为若干段落
  如
  ````
<p> 是一个段落 </p>
<p>这是另一个段落</p>
  ````
  ---
#### 3.HTML折行
在一个段落内进行换行，使用`<br>`
如：
````
<p>这个<br>段落<br>演示了分行的效果</p>
````
---
#### 4.文本格式化
HTML文本格式化标签
````
<b>         定义粗体文本
<em>        定义着重文字
<i>         定义斜体字
<small>     定义小号字
<strong>    定义加重语气
<sub>       定义下标字
<sup>       定义上标字
<ins>       定义插入字
<del>       定义删除字
````
---
#### 5.HTML链接
HTML使用标签 `<a>`来设置超文本链接。
超链接可以是一个字，一个词，或者一组词，也可以是一幅图像，您可以点击这些内容来跳转到新的文档或者当前文档中的某个部分。
##### 超链接语法
 ````
 <a href="https://www.cqjtu.edu.cn/">重庆交通大学</a>
 ````
 ##### HTML 链接 - target 属性
 使用 target 属性，你可以定义被链接的文档在何处显示。
 ````
 <a href="https://www.cqjtu.edu.cn//" target="_blank" rel="noopener noreferrer">重庆交通大学</a>
 ````
 这个会新开窗口进行跳转
 ##### 锚点（页内）
 锚点，也称为书签，用于标记页面的某个元素或位置。通过锚点，我们可以轻易的在长页面内实现跳转。
先使用id属性生成某元素的锚点，然后再使用超链接指向该锚点即可。
````
<a id="tips">有用的提示部分</a>
<a href="#tips">访问有用的提示部分</a>
````
---
#### 6.头部`<head>`
`<head>` 元素包含了所有的头部标签元素。在 `<head>`元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。

可以添加在头部区域的元素标签为: `<title>`, `<style>`, `<meta>`, `<link>`, `<script>`, `<noscript>` 和  `<base>`
````
<head>   定义了文档的信息
<title>  定义了文档的标题
<base>   定义了页面链接标签的默认链接地址
<link>   定义了一个文档和外部资源之间的关系
<meta>   定义了HTML文档中的元数据
<script> 定义了客户端的脚本文件
<style>  定义了HTML文档的样式文件
````
---
#### 7.HTML 图像- 图像标签（ `<img>`）和源属性（Src）
在 HTML 中，图像由<img> 标签定义。
<img> 是空标签，意思是说，它只包含属性，并且没有闭合标签。
要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。
格式如下：
````
<img src="url" alt="some_text">
````
URL 指存储图像的位置。
alt 属性用来为图像定义一串预备的可替换的文本(当图片失效时，用alt指定的文本代替，替换文本属性的值是用户定义的。）
---
####  8.HTML表格
表格由 `<table>` 标签来定义。每个表格均有若干行（由 `<tr>` 标签定义），每行被分割为若干单元格（由 `<td>` 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。
例如
````
<table border="1">
    <tr>
        <td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
    </tr>
    <tr>
        <td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
    </tr>
</table>
````


表格的表头使用 <th> 标签进行定义。
大多数浏览器会把表头显示为**粗体居中**的文本：
 ````
 <table border="1">
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
    </tr>
    <tr>
        <td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
    </tr>
</table>
 ````
 ---
 #### 8.HTML列表
 ##### HTML无序列表
无序列表是一个项目的列表，此列项目使用**粗体圆点**（典型的小黑圆圈）进行标记。无序列表使用 `<ul>` 标签
 ````
<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>
 ````
 
 ##### HTML有序列表
 有序列表也是一列项目，列表项目使用**数字**进行标记。 有序列表始于 <ol> 标签。每个列表项始于 `<li>` 标签。列表项使用数字来标记。
````
<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>
 ````
---
 #### 9.HTML区块
 大多数 HTML 元素被定义为块级元素或内联元素。
块级元素在浏览器显示时，通常会以新行来开始（和结束）。
实例: `<h1>`, `<p>`, `<ul>`, `<table>`
##### `<div>`元素
 HTML `<div>` 元素是块级元素，它可用于组合其他 HTML 元素的容器,它属于块级元素，浏览器会在其前后显示折行。
如果与 CSS 一同使用，<div> 元素可用于对大的内容块设置样式属性。
`<div>` 元素的另一个常见的用途是文档布局。它取代了使用表格定义布局的老式方法。使用 `<table>` 元素进行文档布局不是表格的正确用法。`<table>` 元素的作用是显示表格化的数据。
 如，
 ````
 <!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>

<div id="container" style="width:500px">

<div id="header" style="background-color:#FFA500;">
<h1 style="margin-bottom:0;">主要的网页标题</h1></div>

<div id="menu" style="background-color:#FFD700;height:200px;width:100px;float:left;">
<b>菜单</b><br>
HTML<br>
CSS<br>
JavaScript</div>

<div id="content" style="background-color:#EEEEEE;height:200px;width:400px;float:left;">
内容在这里</div>

<div id="footer" style="background-color:#FFA500;clear:both;text-align:center;">
版权 © runoob.com</div>

</div>
 
</body>
</html>
 ````
 ---
 ##### `<span>`元素
 HTML `<span>` 元素是内联元素，可用作文本的容器
`<span>` 元素也没有特定的含义。
当与 CSS 一同使用时，`<span>` 元素可用于为部分文本设置样式属性。
 如，
 ````
 <!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>
<p>我的母亲有 <span style="color:blue;font-weight:bold">蓝色</span> 的眼睛，我的父亲有 <span style="color:darkolivegreen;font-weight:bold">碧绿色</span> 的眼睛。</p>
</body>
</html>
 ````
 ---
 ##### HTML分组标签
 |标签|描述|
 |:----:|:----:| 
 |`<div>`|定义了文档的区域，块级 (block-level)|
 |`<span>`|用来组合文档中的行内元素， 内联元素(inline)|
 ---
#### 10.HTML表单(`<form>`)
 HTML 表单用于收集用户的输入信息，表示文档中的一个区域，此区域包含交互控件，将用户收集到的信息发送到 Web 服务器。
表单是一个包含表单元素的区域，允许用户在表单中输入内容，
 比如：文本域（textarea）、下拉列表（select）、单选框（radio-buttons）、复选框（checkbox） 等等。
 ##### 输入元素
 多数情况下被用到的表单标签是输入标签 `<input>`。
输入类型是由 type 属性定义。
接下来我们介绍几种常用的输入类型。
 **文本域**
 文本域通过 `<input type="text">` 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域。
````
 <form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>
 ````
 ---
**密码字段**
密码字段通过标签 `<input type="password"> `来定义:
实例
 ````
<form>
Password: <input type="password" name="pwd">
</form>
 ````
 ---
 **单选按钮（Radio Buttons）**
`<input type="radio">` 标签定义了表单的单选框选项:
实例
 ````
<form action="">
<input type="radio" name="sex" value="male">男<br>
<input type="radio" name="sex" value="female">女
</form>
 ````
 ---
 **复选框（Checkboxes）**
`<input type="checkbox"> `定义了复选框。
复选框可以选取一个或多个选项：
实例
 ````
<form>
<input type="checkbox" name="vehicle" value="Bike">我喜欢自行车<br>
<input type="checkbox" name="vehicle" value="Car">我喜欢小汽车
</form>
 ````
 ---
 **提交按钮(Submit)**
`<input type="submit">` 定义了提交按钮。
当用户单击确认按钮时，表单的内容会被传送到服务器。表单的动作属性 action 定义了服务端的文件名。
action 属性会对接收到的用户输入数据进行相关的处理:
实例
 ````
<form name="input" action="html_form_action.php" method="get">
Username: <input type="text" name="user">
<input type="submit" value="Submit">
</form>
 ````
 ---
 综合上述元素，例子如下
 ````
 <form>
  <!-- 文本框，注意有 placeholder 提示符 -->
  用户名：<br>
  <input type="text" name="name" placeholder="请输入用户名"><br>
  <!-- 密码框 -->
  密码：<br>
  <input type="password" name="ps" placeholder="请输入密码"><br>
  年龄：<br>
  <!-- 数字输入框，注意 min 和 value 属性-->
  <input type="number" name="age" min="18" value="18"><br>
  <!-- 单选按钮, 注意 checked 属性 -->
  性别：<br>
  <input type="radio" name="gender" value="male" checked> 男<br>
  <input type="radio" name="gender" value="female"> 女<br>
  <input type="radio" name="gender" value="other"> 其它<br>
  <!-- 下拉列表，注意 selected 属性 -->
  党派：<br>
  <select name="party">
    <option value="D">民主党</option>
    <option value="R" selected>共和党</option>
    <option value="N">无党派</option>
  </select><br>
  <!-- 多选框 -->
  您有哪些交通工具：<br>
  <input type="checkbox" name="vehicle1" value="Bike"> 自行车<br>
  <input type="checkbox" name="vehicle2" value="Motocycle" checked> 摩托车<br>
  <input type="checkbox" name="vehicle3" value="Car"> 轿车<br>
  <input type="checkbox" name="vehicle4" value="Jet"> 飞机<br>
  <!-- 日期选择器 -->
  您的工作日期：<br>
  <input type="date"><br>
  <!-- 文件选择器 -->
  上传您的照片:<br>
  <input type="file" name="photo"><br>
  <!-- 文本输入区域，注意 rows 和 cols 属性 -->
  您的建议：<br>
  <textarea name="message" rows="5" cols="30">
    The cat was playing in the garden.
  </textarea><br><hr>
  <!-- 表单提交/重置按钮，将表单中的数据取消或传输给服务器端进行处理 -->
  <input type="submit" value="提 交">
  <input type="reset" value="重 置">
</form>
 ````
$\color{red}{注：}$
 当提交时，表单中没有`name`属性的元素将不会提交，比如上面工作日期的选择器。有`name`属性的元素其`value`的值将提交给服务器。
---
 
