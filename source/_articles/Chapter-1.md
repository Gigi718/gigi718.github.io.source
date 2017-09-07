---
title: Chapter 1
date: 2017-09-07 13:47:07
categories:
tags: [JavaScript权威指南]
skip: false
---
## 1.1JavaScript语言核心
#### 重点内容
//  所有在双斜杠后的内容都表示注释   
//  变量是表示值的一个符号名字  

//  变量是通过var关键字声明的   
`var x;`    //  声明一个变量x  

//值可以通过等号赋值给变量  
`x = 0;`    //  现在变量x的值为0 
 
//  JavaScript支持多种数据类型  
`x = 1;`        //  数字  
`x = 0.01;`     // 小数  
`x = "hello world";`    //  由双引号内的文本构成的字符串  
`x = 'JavaScript';`     //  单引号内的文本同样构成字符串  
`x = true;  
 x = false;`    //  两个布尔值  
`x = null;`     //  null是一个特殊的值,意思为"空"  
`x = undefined;`    //  undefined和null非常相似  


**JavaScript中两个非常重要的类型就是对象和数组。**  
//  JavaScript中最重要的类型就是对象  
//  对象是名/值对的集合,或字符串到值映射的集合  
```
var book = {                // 对象是由花括号括起来的
    topic : "JavaScript",   // 属性"topic"的值是"JavaScript"
    fat = true              // 属性"fat"的值是true
};                          // 右花括号标记了对象的结束  
```
 
//  通过"**.**"或"**[ ]**"来访问对象属性  
`book.topic`    //  → "Javascript"  
`book["fat"]`   //  → true:另外一种获取属性的方式
