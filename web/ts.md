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
在TS中使用这个是会进行报错的
````
money=[100,"美元"];
````


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

---
# 五.解构
为了方便使用，我们可以将对象，数组的元素解构到变量中(感觉有点像元组的使用)。
````
//数组
let dog=["puppy","happy","bas"];
let [one,...others]=dog;
alert(...others);

//对象（变量名要和对象中的一样）
let dog={
age:5,
name:"puppy",
color:"blue"
}
let {age,color}=dog;
alert(a+" "+b);
````

# 六.类
类和其他语言一样是属性与函数的集合，
与面向对象的写法基本上差不多。
### 1.定义
````
class Dog{
//属性
age: number;
color: string;
name: string;
//构造函数
constructor(age:number,color:string,name:string){
this.age=age;
this.color=color;
this.name=name;
}
//类的函数
printAll(): void{
alert(this.age+" "+this.color+" "+this.name);
}
}
//创建对象
let ss = new Dog(2, 'blue', 'puppy');
//使用类的函数
ss.printAll();
````

### 2.继承(extends)
同我们经常使用面向对象一样，TS允许继承来扩展现有的类

````
//基类

class Dog {

    age: number;
    color: string;
    name: string;

    constructor(age: number, color: string, name: string) {
        this.age = age;
        this.color = color;
        this.name = name;
    }
}
//子类
class labuladuo extends Dog{
constructor(age:number,color:string,name:string){
    super(age, color, name);
}
playHappy():void{
alert("play happy");
        }
}
let labu = new labuladuo(5, "blue", "haha");
labu.playHappy();
````

### 3.属性和函数的访问权限
和其他语言一样，访问权限修饰符分别是public,private,protected.

**注**：如果没有写权限的话，默认是public

public 全局都可以访问

private只能在这个类里面访问，子类也不能访问

protected 在类的内部和子类的内部都可以访问到

不过还有只读权限（readonly）,使用这个属性时只能在声明和构造函数中进行初始化，其他操作无法修改值。
````
class Dog{
age: number;
color: string;
readonly name: string;

constructor(age:number,color:string,name:string){
this.age=age;
this.color=color;
this.name=name;
}

printAll(): void{
alert(this.age+" "+this.color+" "+this.name);
}
}
//创建对象
let ss = new Dog(2, 'blue', 'puppy');
//使用类的函数
ss.name="sss";//会报错

````

### 4.存取器(getter setter)
当类的属性设置成private时，需要在类外部读取和修改private属性，需要用到getter和setter操作
````
class Dog{
 age: number;
private _color: string;
private  _name: string;

constructor(age:number,color:string,name:string){
this.age=age;
this._color=color;
this._name=name;
}

set name(value:string){
this._name=value;
}

set color(value:string){
this._color=value;
}

get name():string{
return this._name;
}

get color():string{
return this._color;
}

printAll(): void{
alert(this.age+" "+this._color+" "+this._name);
}
}
````

### 5.静态属性(static)
用static定义的类和属性可以直接使用不需要生成具体的对象
````
class Dog{
age: number;
color: string;
name: string;

constructor(age:number,color:string,name:string){
this.age=age;
this.color=color;
this.name=name;
}
//类的函数
static printAll(): void{
alert("happy!!!");
    }
}

Dog.printAll();
````

# 七.泛型
使用泛型就可以让组件支持多种数据类型，可以让组件重复性使用。

有点像c++中的模板类和模板函数

### 1.泛型函数
````
function 函数名<泛型>(参数: 泛型): 返回类型{

}
````
比如
````
function Dog<T>(name: T):T{
return name;
}
let ss=Dog("sssss")
alert(typeof(ss))
let sss=Dog(123)
alert(typeof(sss))

````
对于泛型类型的使用要注意类型中有一些属性是不通用的，比如说number类型没有.length属性。

于是我们可以把参数设置成泛型数组，这样传入数字的话，返回的数字数组，就有.length属性了。

我们可以通过把泛型变量当作类型的一部分使用来增强灵活性
````
function Dog<T>(name: T[]):T[] {
alert(name.length)
return name;
}
````

### 2.泛型类
````
/*
class 类名<泛型类型>{
......
}
*/


class Samples<T>{
      values: T;
      prinstall():void{
         alert(this.values)
     }
}
let simples = new Samples<number>();
simples.values = 123;
simples.prinstall();
````

# 八.模块
当项目很大时，如果将所有代码都写在一起无疑是很恼火的。于是需要使用模块进行管理。

由于模块只在自身范围内起作用，对模块外部是不可见的。所以我们需要使用$\color{red}{export}$来导出，
也需要用$\color{red}{import}$来导入(**必须要一起使用**，不暴露的话没法引入，不引入的话没法使用)
````
//Dog.ts
//export 暴露这个类
//export 类...
export class Dog{
        name:string;
        age:number;
     printall(): void {
            alert(`this dog is ${this.age} and name is ${this.name}`)
     }
}


//main.ts
//导入Dog.ts模块(import),后缀(.ts)默认去掉
//import {模块} from 位置


import {Dog} from ../Dogs/Dog;
let a = new Dog();
a.name = "puppy"
a.age = 12;
a.printall();
````

























