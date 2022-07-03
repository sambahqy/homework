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

注意：NaN 表示保留字，说明不是数字;
      undefined 表明对象属性or方法不存在or声明了变量但未赋值;
      null 空。


### 4.操作符
|操作符| |
|:----:|:----:| 
 |赋值，算术和位运算符	|=  +  -  *  /	|
 |布尔操作符|&&  !  \|\| |
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

# 五.对象
js的对象和python差不多，以键值对的方式进行书写，还可以在里面写对象函数，比如：

````
var dog={
    name:"poppy",
    age:3,
    color:"white"
   function ss(){
   alert("sssss");
   }
};
````
当访问对象某个元素时可以直接指到这个元素的名字，比如：
````
alert(dog.age);
````

不过对于大工程的书写，就是这类对象的实体非常多的话如果按照这么写就会非常的麻烦。

我们可以通过建立个函数，返回类型是对象类型，再把该对象的属性传进去，把这个对象写的自定义函数写进去就可以形成一个对象模板

如：
````
.....上面的dog类为例

function dogs(name,age,color){
var s=new Object();
s.name=name;
s.age=age;
s.color=color;
 s.ss=function{
   alert("sssss");
   }
 retrun s;
}

````

# 六.函数
函数的格式基本和python类似，关键字不过不一样。格式如下：
````
function 函数名(参数)
{
    函数体....
    
    返回类型  return 值;
}
````
当然，你可以没有返回值和参数，不过需要**注意**的是

1.不管你输入多少个参数，多的话函数总是取与参数个数相同的前N个，少的话也不管，反正就是不会给你报错；

2.对于函数名字一样的函数，总是调用最后一个函数名一样的。

### 箭头函数
 箭头函数可以让我们写的函数更加简洁，比较适合那些匿名函数的地方
````
var 名称=(参数)=>{内容};
````
比如
````
var s="小明";
var happy=(s)=>{happy+s};
````
注意：如果只有一个参数，可以省略参数的括号。如果函数体只有一个语句，也可以去掉大括号和return

# 七.数组
JS中的一个数组是可以存放多个类型的值，所以数组的大小会自动调整。比如：
````
var dog = ["wangcai", "male", 5];
````
其实数组就是一种特殊的对象，你用typeof进行类型查看的时候会发现弹出来的是object类型。

如果在数组中填入或输出多个类型的元素，有可能会因为类型问题出错，毕竟JS在语法上比较松散。

比较建议一个数组一个类型，多个类型用对象。

## 数组的一些方法
### 1.转换成字符串（toString）
````
var dog = ["wangcai", "male", 5];
alert(dog.toString());
````

### 2.join()
join可以改变数组的分隔符
````
var dog = ["wangcai", "male", 5];
alert(dog.jion("%"))
````
### 3.栈操作（push ,pop）
可以将数组看作一个栈，进行先进后出的操作

````
var dog = ["wangcai", "male", 5];
dog.push("blue");
var m=dog.pop();
alert(m);
````
### 4.队列操作(push,shift)
也可以将数组看作队列进行操作，先进先出

````
var dog = ["wangcai", "male", 5];
dog.push("blue");
var m=dog.shift();
alert(m);
````
### 5.更改操作
可以通过数组下标找到对应的元素进行更改
````
var dog = ["wangcai", "male", 5];
dog[2]=10;
````
### 6.删除操作(delete)
也是通过数组下标来进行删除

````
var dog = ["wangcai", "male", 5];
 delete dog[2];
````

### 7.拼接操作(concat)
将两个数组连在一起，形成新的数组
````
var dog = ["wangcai", "mal"];
var bri = ["2"];
var dogs = dog.concat(bri); 
````

### 8.splice（）
splice可以对数组进行增，删，改的操作。








### 9.裁剪数组(slice)
其实就是和python的切片操作类似，将裁剪的部分当作新的数组（不影响原数组）
````
//slice(起始位置，结束位置)
//取出来的不包括结束位置的值


var dog = ["wangcai", "male", 5,"red","puppy"];
var s=dog.slice(1,4)
````













