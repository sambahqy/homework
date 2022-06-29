# 一. CSS简介
CSS 是层叠样式表，定义如何显示 HTML 元素，即进行html页面的美化，让页面更具有美感。此外样式与内容可以进行分离，我们可以把样式保存在外部的CSS文件中就行（方便修改）

---
# 二.CSS语法
CSS规则主要是由两个主要部分构成：选择器和一个及多个声明语句，例如：
```
div {
      color:blue;
      text-aligin:center;
}
```
每一条的声明都由;结尾，所有的声明都要写在{}里面

---
# 三.CSS三种创建方法
css有三种创建方法，分别是：外部样式表，内部样式表，内联样式。

 $\color{red}{优先级：}$ 内联样式>内部样式表>外部样式表>浏览器默认样式
 
### 1.外部样式表
外部样式表是将样式写在.css文件中，与html文件分开。方便对样式进行修改，且具有一定的可重复使用性。
当然在外部写了的.css样式要应用于html文件需要与`<link>`来链接（一般放到文档头部）
```
<link rel="stylesheet" type="text/css" href="位置">
```

### 2.内部样式表
内部样式表是将你写的样式就放入HTML文件中，一般是放在头部那里，写在`<style></style>`里面。例如：
```
<style>
hr {
    color:blue;
}
body {
    padding:0
}
</style>
```

### 3.内联样式
直接将样式写入标签里面，标签里面需要用这种格式：style:""。例如
```
<p style="color:blue;">嘀嘀嘀</p>
```
---
# 四.CSS一些常用样式

### 1.背景

#### 背景颜色
```
p {
background-color:blue;
}
```
#### 背景图片（默认是平铺覆盖显示）
```
div{
background-image:blue: url('图片位置')
}
```
如果要对垂直或水平平铺进行修改，则需要加上一句（垂直平铺举例）：
```
background-repeat: repeat-y
```
至于里面可以填哪些，可以自行了解（no-repeat,repeat-x....）。

设置位置的话用 ***background-position: ;***

### 2.文本

#### 文本颜色
```
h1 {
      color:#blue;
}
```

#### 文本对齐（左，右，居中,两端对齐）
````
text-align: right;
````
#### 文本修饰(多是用于删除链接的下划线的)
````
a {
      text-decoration:none;
}
````

### 3.元素内容大小(height，width)
通过使用这两个元素来调整大小，常用单位是：px(像素),%(百分比)
````
div {
  height: 100px;
  width: 500px;
 
}
````
### 4.不透明度(opacity)
使用opacity属性进行图片的不透明度的设计，属性值是0.0~1.0，**值越小越透明**
````
img{
  opacity:0.5;
}
````

---
# 五.盒子模型
[![盒子图标](https://www.runoob.com/images/box-model.gif)

Margin(外边距)---与其他元素的距离

Border(边框)-----边框（一般不显示）

Padding(内边距)--与content之间的距离的区域

Content(内容)----显示文本，图像等

例如：

````
div {
    width: 350px;
    border: 20px blue;
    padding: 20px;
    margin: 20px;
}
````
---
### 1.边框（border）

#### 边框样式(border-style)
定义边框长啥样，比如无边框，虚边框，点线边框等等，例如
````
div {
      border-style: dotted;
}
````

#### 边框颜色( border-color)
````
div{
      border-style: solid;
      border-color: blue;
}
````

#### 边框宽度（ border-width）
````
div{
      border-style: solid;
      border-color: blue;
       border-width： 20px;
}
````
### 2.外边距(margin)
用简写模式（上右下左，顺时针方向设置样式）为例
````
margin:10px 60px 80px 20px;
````
### 3.内边距(padding)
内边距是内容与边界距离之间的区域，与外边距简写模式(上右下左)一样，例如：
````
padding:20px 40px 80px 50px;
````
---
# 六.定位（position）
定位属性指定了元素的定位类型，有五个值 ***static，relative，fixed，absolute***

### 1.static(静态)
是HTML的默认值，遵循正常的文档流对象，不会受到top,right,botom,left影响
````
div{
      position:static
      
}
````

### 2.relative(相对)
相对定位是相当于原本正常的位置(static)进行的
````
div{
    position:relative;
    top:-50px;
}
````

### 3.fixed（固定）
这个是定位是相当于浏览器窗口(视口)的，是固定位置(窗口滚动也不会移动)
````
p{
    position:fixed;
    top:30px;
    right:10px;
    color:blue;
}
````

### 4.absolute（绝对）
位置相对与设置了定位的父元素(**非静态(static)**)
````
<!-- style -->
p{
    position:absolute;
    left:100px;
    top:150px;
    color:blue;
}

div{
    position: relative;
    width: 20px;
    height: 20px;
}

<!-- style -->
<!-- html -->
<div>
<p>123456789</p>
</div>
<!-- html -->
````

# 七.overflow(溢出)
用于控制内容溢出元素框时候对溢出的部分进行处理。
对应的值有：

 |值|描述|
 |:----:|:----:| 
 |visible|默认，超出部分仍会显示)|
 |hidden|会被裁剪，被裁部分内容不可见|
 |scroll|会被裁剪，可以滑动滚动条见到|
 |auto|会被裁剪，看视情况提供滚动条|

例如
````
div {
    width: 10px;
    height: 22px;
    background-color: blue;
    overflow: hidden;
}
````

# 八.float（浮动）
float会使元素向左或向右移动，其周围的元素也会重新排列(往往用于图像，布局)。
浮动一般是水平方向移动，外边缘碰到包含框或另一个浮动框的边框为止。
浮动元素之后的元素将围绕它。
例如：
````
div{
    width:100px;
    height:100px;
    margin:10px;
    float:left;
}
````
注：1.如果将几个浮动的元素放在一起，如果有空间的话会彼此相邻
    2.如果要清除浮动效果的话，则需要使用 clear:both;  语句

---
# 九.组合选择器
css有三种选择器：**元素，id,class**。
我们可以对这些进行组合，达到对某一个或者某一种进行专门的样式设及把这几个选择器进行一个组合。
这里介绍两种普遍的选择器：后代选择器，子元素选择器

### 1.后代选择器
用于取某个元素的后代元素，例如：
````
div h1
{
  color:blue;
}
````

### 2.子选择器
子元素选择器只能选择作为某元素直接or一级子元素的元素，例如
````
div>h1
{
  color:blue;
}
````
---

# 10.伪类与伪元素
伪类和伪元素是用来对选择器来添加一些特殊的效果，比如点击链接后颜色的不同展示
````
a:link {
      color:grey;
} 
a:visited {
      color:blue;
} 
````

### 语法如下
选择器: 伪类or伪元素 {}

例如下面使用伪元素让后行变红
````
p:first-line {
    color:red;
}
````



