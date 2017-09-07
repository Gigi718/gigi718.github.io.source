---
title: <Head first java>学习笔记二
date: 2017-08-21 12:11:55
categories:
tags: [Head first java]
skip: false
---
# 对象和对象的引用 
1. 何谓对象?  
- 要理解什么是对象就要结合类一起理解
- 每个对象都是每个类的实例(instance),这里,"类"就是"类型"的同义词。类相当于人类,而"张三"就是独享,相当于"人类"的实例。  

2. 何谓对象引用? 
- 在Java里,一切都被"看作"对象,但**操纵的标识符实际上是指向一个对象的"引用(reference)"**。  
- 对象和对象引用不是一回事,是两个完全不同的概念。  
`Person person = new person('张三');`  
相当于:  
`Person person;`  `//声明一个Person类的引用`    
`person = new person('张三');`      `//创建一个名为"张三"的新对象`   
这两行代码实现的功能和上面的一行代码是完全一样的。  
在Java中,**new是用来在堆上创建对象用的**,由此可见,person并不是所创建的对象。上面说  
"**操纵的标识符实际上是指向一个对象的引用**"  
也就是说,person是一个引用,是指向一个可以指向Person类对象的一个引用  
真正创建对象的语句是右边的`new person("张三")`。  

**一个引用可以指向多个对象**  
`Person = person`  
 `person = new person('张三');`  
 `person = new person('李四');`  
 **一个Person类的引用,它可以指向任何Person类的实例(不止一个)**  
 **同样的,一个对象也可以被多个引用所指**  
 `Person person1 = new person('张三');`
 `Person person2 = person1;`  
 
# 控制`Dog`类型
方法: 通过引用变量的来存取Dog的实例变量与方法
引用变量通过使用圆点运算符来存取Dog的实例变量与方法。  
`Dog fido = new dog();  //声明一个名为fido的对象并定义为Dog类型的变量`  
`fido.name = 'fido';    //通过圆点运算符来读取变量fido的值name`  
# 通过数组来存取`Dog`数组中的`Dog`
**注意事项**   
- 对数组的操作不需要变量名称
- 在数组中是通过数组的索引来操作特定对象  
`Dog[] myDogs = new Dog[3];     //声明一个名为myDogs的Dog数组并设定成员数量为3`  
 `myDogs[0] = new Dog();    //创建数组的第一个成员`  
 `myDogs[0].name = 'fido';  //读取数组中第一个成员的name值为'fido'`  
 