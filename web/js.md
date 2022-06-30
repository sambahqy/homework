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
# 四.JS基本语法

### 1.关键字
关键字就和其他语言一样，不能被用作变量名。JS的关键字如下：

abstract   else    instanceof     super       boolean  	enum    	int  	   switch

break	    export  	interface 	synchronized     byte  	 extends  	let	     this

case	     false     	long       	throw         catch   final  	 native	   throws

char	     finally	   new	       transient      class   	float   	null    	true

const     	for     	package	      try        continue 	function 	private	 typeof

debugger	  goto   	protected     	var         default	    if    	public	   void

delete	 implements  	return     	volatile       do	     import   	short   	while

double	    in	      static       	with


### 2.变量
 var 来定义变量，不过这里注意var 定义的变量的类型随赋值的数据类型进行改变。
 这里就会感觉数据类型的判断有点恼火。
 ````
 var a=10;
 alert(a);
 a="1234"
 alert(a);
 ````
**注意：** 这里的变量和其他语言一样，存在着局部变量，当一个函数结束完成后也会被回收掉

### 3.数据类型
JS有很多个数据类型，这里列举几个常见的
数字（number），字符串（String），数组（Array），对象(Object)
````
var l = 10;                                       //number
var names = "hhhhh";                              // String 
var phone = ["Saxing", "apple", "huaiwei"];       // Array  
var dog = {yanse:"blue", daxiao:"da"};            // Object 
````

### 4.操作符
|操作符| |
|:----:|:----:| 
 |赋值，算术和位运算符	|=  +  -  *  /	|
 |布尔操作符|&&  !  \| \| |
 |关系操作符| <> <=>= == === != !==|

**注意：**

1.布尔操作符判断为假的值： false、null、undefined、''、0、NaN 

2.对于关系运算符的全等（===），这才是进行比较使用的，使用 == 的话会将比较的值转换为字符型再去比较。

例如：
````
var s='11111'
alert(s==11111)
alert(s===11111)
````

# 五.语句
JS的语句和其他语句的关键字基本一致，比如 if,break,do...while,for之类的
不过我觉得与python语言相似程度很高
对于循环遍历来讲的话和python感觉差不多，有好几种遍历的方法

















