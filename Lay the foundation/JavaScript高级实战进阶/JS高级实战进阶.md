# JS高级进阶

## 1_基础总结深入

## 001-分号问题

<img src="F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\分号问题.png" style="zoom:50%;" />

### 01_数据类型

1.分类

​	基本值类型

- String:值是任意的字符串
- Number：值是任意数字
- boolean：true /false
- undefined：本身
- null：本身		

​	对象（引用）类型

- Object：任意对象
- Function：一种特别的对象（可以执行的对象）
- Array：一种特别的对象（数值下标，内部数据是有序的）

2.判断

- typeof：返回对应的字符串（不能判断null/undefined  object/array）

- [instanceof](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/instanceof)：判断对象的具体类型（是对象？数组？函数？）

- === / == ：前者判断完全相等，后者不可以，会进行类型转换

  typeof null 的返回值是Object，判断null使用===（nudefined也一样）

**什么是实例：实例对象的简写  **   **什么是类型：类型对象的简写**

```js
function Person (name,age){//构造函数 类型
    this.name=name;
    this.age=age;
}
const p = new Person();//根据类型创建的实例对象

Person('jack',12)//语法和法，但不是实例对象，一般不会这么做
```

- undefined和null的区别

  `undefined代表未定义，null代表定义了但是值为null`

- 什么时候要给变量赋值为null呢

  `表明一个未赋值的对象（typeof null 的返回值为Object）`

  ```js
  var b = null;//初始赋值为null，代表将要赋值为对象
  //确定对象就赋值
  b = ['atguigu',12];
  //最后
  b = null;//让b指向的对象成为垃圾对象（垃圾回收器回收）
  ```

- 严格区别变量类型和数据类型？

  *数据的类型

  ​	*基本类型

  ​	*对象类型

  *变量的类型（变量内存值的类型）

  ​	*基本类型

  ​	*引用类型

## 2数据-变量-内存

### 1.问题：var a = xxx, a中到底保存的是什么？

- xxx是基本数据，保存的就是这个数据
- xxx是对象，保存的是对象的地址值
- xxx是一个变量，保存的xxx的内存内容（可能是基本数据，也可能是地址值）

### 2.关于引用变量赋值的问题

- 2个引用变量指向同一个对象，通过一个变量修改对象内部数据，另一个变量看到的是修改后的数据

### 3.在js调用函数时传递变量参数时，是值传递还是引用传递

<img src="F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\在js调用函数时传递变量参数时，是值传递还是引用传递.png" style="color: red; zoom: 50%;" />

### 4.js引擎如何进行内存管理？

<img src="F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\4.js引擎如何进行内存管理？.png" style="zoom:50%;" />

## 3.对象

<img src="F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\对象.png" style="zoom:50%;" />

### 问题：什么时候必须使用['属性名']的方式？

<img src="F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\问题：什么时候必须使用['属性名']的方式？.png" style="zoom:50%;" />

## 4.函数

### 1.函数

<img src="F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\1.函数.png" style="zoom:50%;" />

### 2.回调函数

![](F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\2.回调函数.png)

### 3.IIFE

<img src="F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\IIFE.png" style="zoom: 50%;" />

### 4.原型

<img src="F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\原型1.png" alt="原型1"  />

![](F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\原型2.png)

### 5.显性原型与隐形原型

![](F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\原型4.png)

![](F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\原型3.png)

![](F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\原型5.png)

### 6.执行上下文

![](F:\github本地仓库\atguigu-prprpr\Lay the foundation\JavaScript高级实战进阶\images\上下文.png)
