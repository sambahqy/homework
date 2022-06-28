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
---
# 五.盒子模型
[![RUNOOB 图标](https://www.runoob.com/images/box-model.gif)



