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