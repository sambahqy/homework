# 一.JavaScript简介
JavaScript是一种可以插入HTML页面，轻量级的脚本语言。让页面更具有行为

页面就好比一个鸟，HTML让它具有了骨架，CSS让他有了外貌，JS让他可以飞。

---
# 二.用法
在HTML中使用JS需要放到`<script></script>`中，当然也可以写在.js文件中，链接到HTML中
例如：
```
<script>
alert("111111")
</script>
```
---
# 三.JS输出
JS有四种输出方式，如下：
|方式|表现|
|:----:|:----:| 
 |window.alert()|警告框|
 |innerHTML|写到HTML标签显示的地方|
 |document.write()|写到 HTML 文档|
 |console.log()|写到控制台|

### 1.window.alert()
````
<script>
window.alert("sssssssssssssssss");
</script>
````
### 2.innerHTML
````
<p id="ppp">54321</p>

<script>
document.getElementById("ppp").innerHTML ="12345";
</script>
````
### 3.document.write()
````
<script>
document.write("123456")
</script>
````
### 4.console.log()
在控制台上显示
````
<script>
console.log("console!!!");
</script>

````

---
# 四.
