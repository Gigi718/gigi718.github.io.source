---
title: Chapter 1
date: 2017-09-07 13:47:07
categories:
tags: [JavaScript权威指南]
skip: false
---
##  1.1 JavaScript语言核心

**// 所有在双斜杠后的内容都表示注释**   
**// 变量是表示值的一个符号名字**  

**//  变量是通过var关键字声明的**   
```
var x;    //  声明一个变量x  
```

**//值可以通过等号赋值给变量**  
```
x = 0;   //  现在变量x的值为0 
```
 

**// JavaScript支持多种数据类型** 
```
x = 1;        //  数字  
x = 0.01;     // 小数  
x = "hello world";    //  由双引号内的文本构成的字符串  
x = 'JavaScript';     //  单引号内的文本同样构成字符串  
x = true;  
x = false;    //  两个布尔值  
x = null;     //  null是一个特殊的值,意思为"空"  
x = undefined;    //  undefined和null非常相似  
```

**JavaScript中两个非常重要的类型就是对象和数组。**  

```
// avaScript中最重要的类型就是对象  
// 对象是名/值对的集合,或字符串到值映射的集合

var book = {                // 对象是由花括号括起来的
    topic : "JavaScript",   // 属性"topic"的值是"JavaScript"
    fat = true              // 属性"fat"的值是true
};                          // 右花括号标记了对象的结束  
```
 
//  **通过"**.**"或"**[ ]**"来访问对象属性**  
```
    book.topic             //  → "Javascript"  
    book["fat"]           //  → true:另外一种获取属性的方式
    book.author = "Flanagan";       // → 通过赋值创建一个新属性
    book.contents = {};     //  → {}是一个空对象,它没有属性
```  

**//  JavaScript同样支持数组(以数字为索引的列表)**  
```
var primes = [2,3,5,7];     // 拥有4个值的数组,由"["和"]"划定边界 
primes[0];                  // → 2: 数组中的第一个元素(索引为0)
primes.length               // → 4: 数组中的元素个数
primes[primes.length - 1]   // → 7: 数组中最后一个元素
primes[4] = 9;              // 通过赋值来添加新元素
primes[4] = 11;             // 通过赋值来改变已有元素
var empty = [];             // []是空数组,它具有0个元素
empty.length                // → 0 
```

**// 数组和对象中都可以包含另一个数组或对象:**
```
var points = [                  // 具有两个元素的数组
    {x: 0, y: 0},               // 每个元素都是一个对象
    {x: 1, y: 1}
]
var data = {                    // 一个包含两个属性的对象
    trial1: [[1,2],[3,4]],      // 每一个属性都是数组
    trial2: [[2,3],[4,5]]       // 数组的元素也是数组
}
```


**以上通过方括号定义数组元素和通过花括号定义对象属性名和属性值之间的映射关系的语法成为初始化表达式(initialize expression)。  
表达式是JavaScript中的一个短语,这个短语可以通过运算得出一个值。通过"."和"[]"来引用对象属性或数组元素的值就构成一个表达式。**  

JavaScript中最常见的表达式写法是像下面代码这样使用运算符(operator):  

```
// 运算符作用于操作数,生成一个新的值
// 最常见的是算术运算符
3 + 2           // → 5: 加法
3 - 2           // → 1: 减法
3 * 2           // → 6: 乘法
3 / 2           // → 1.5: 除法
points[1].x - points[0].x       // → 1: 更复杂的操作数也能照常工作
"3" + "2"       // → 32: + 可以完成加法运算也可以作字符串连接
```

**// JavaScript定义了一些算数运算符的简写形式**
```
var count = 0;                  // 定义一个变量
count++;                        // 自增1
count--;                        // 自减1
count += 2;                     // 自增2
count *= 3;                     // 自乘3
count                           // →  6:变量名本身也是一个表达式
```

**// 相等关系运算符用来判断两值是否相等**  
**// 不等、大于、小于运算符的运算结果是true或false**
```
var x = 2 ,y = 3;               // 这的 = 等号是赋值的意思,不是比较相等
x == y;                         // → false: 相等
x != y;                         // → true: 不等于
x < y;                          // → true: 小于
x <= y;                         // → true: 小于等于
x > y;                          // → false: 大于等于
x >= y;                         // → false: 大于等于
"two" == "three"                // → false: 两个字符串不相等
"two" > "three"                 // → true: "tw"在字母表中的索引大于"th"
false == (x > y)                // → true: false和false相等
```

**// 逻辑运算符是对布尔值的合并或求反**
```
(x == 2) && (y == 3)            // → true: 两个比较都是true,结果为true
(x > 3) || (y < 3)              // → false: 两个比较一个为true结果就是true,两个都为false结果才是false
!(x == y)                       // → true: ! 求反
```
