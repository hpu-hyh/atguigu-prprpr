# JS高级进阶

## 1_基础总结深入

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
