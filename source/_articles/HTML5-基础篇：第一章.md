---
title: HTML5-基础篇：第一章
date: 2017-09-12 18:46:07
categories:
tags: [妙味课堂]
skip: false
---
#### 常见样式-边框
边框粗细    1px  
边框样式    style(solid dashed )  
边框颜色    color(red yello green)  
边框的形状   非矩形  
##### 使用边框实现三角形
```
    width:0px;
    height:0px;
    border:5px solid red;
    border-top-color:green;
```


#### 常见样式-背景 background
内容是会撑开容器宽高、背景不会占用容器宽高  
```
background-color    背景颜色  
background-image    背景图   
background-image:url(img/1.jpg)      背景图引用路径   
```
背景图默认铺满整个背景
##### background-repeat 背景平铺   
```
background-repeat           背景重复
   no-repeat     不重复  
   repeat-x      x轴重复
   repeat-y;     y轴重复
   repeat;       x、y轴都重复
```
##### 背景图定位
```
background-position:x y;        背景定位  
    具体数值
    方向 left right center
    top bottom center
当第二个属性值没有填写的时候,默认居中。
```
##### 背景图是否滚动
```
background-attachment       背景图是否滚动
    fixed       固定在浏览器可视区域
    scroll      跟随滚动条滚动
    
```
##### 背景图复合样式