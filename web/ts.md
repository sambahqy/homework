# 一.Typescript安装
在安装好node.js后，用管理员身份打开cmd

输入(-g 全局安装)
````
npm -g install ts-node typescript
````
---
# 二.TS简介
TS是微软开发的开源的语言，在JS的基础上添加静态类型构成的。
可以在任何浏览器，任何操作系统使用

---
# 三.变量
TS中使用let,const来代替JS中的var，这样就可以避免由于var声明的难以理解的作用域规则带来的问题

### 1.let 
let的写法和var一样，不过作用域是块级的({})

不过使用的话最好加上类型（虽然也可以自动推断出来）
````
let age : number=23;
````

### 2.const
const来声明变量，那个变量的值就不能修改（相当于常量）

使用与let差不多
````
let name: string="happy";
````
# 四.基础类型
TS几乎支持JS相同的数据类型(number,string,boolean...)

此外还提供了枚举类型

这里总结几个JS中没有的数据类型

### 1.元组
元组可以表示已知元素数量和类型的数组，例如
````
let money:[string,number];
money=["美元",100];

````
虽然在JS中使用
````
money=[100,"美元"];
````
也是对的，但是在TS中是会进行报错的。

### 2.枚举(enum)
你可以通过枚举名字来获得值，也可以枚举值来获得对应的名字(**对应的值必须是数字的**)。
````
enum dog {
puppy=2,
happy=3,
bads=5
}
let m: dog=god.puppy;
let s:string =dog[3]
````
其实就相当于给这些名称赋了个下标，通过元素查下标，也可以通过下标查元素


























