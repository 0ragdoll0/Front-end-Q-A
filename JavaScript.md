1. 介绍js的基本数据类型。
>     Undefined Null Boolean Number String
>     ES6新增Symbol，定义后独一无二且不变的数据类型

2. 介绍js有哪些内置对象？
>     数据封装类对象：Object、Array、和基本包装类型(Boolean Number String)
>     其他对象：Date、RegExp、Function、Arguments、Math、Error

3. 说几条写JavaScript的基本规范？
>     请使用 ===/!==来比较true/false或者数值（避免数值转换后的比较）
>     Switch语句必须带有default分支
>     For循环必须使用大括号
>     If语句必须使用大括号
>     for-in循环中的变量 应该使用var关键字明确限定作用域，从而避免作用域污染。

4. JavaScript有几种类型的值？，你能画一下他们的内存图吗？        
> 基本数据类型（undefined，null，boolean，number，string）和引用数据类型（object）       
> 基本数据类型具有固定的内存大小，属于频繁使用数据，在栈中储存。        
> 引用数据类型没有固定的内存大小，放在栈中会影响程序运行性能。寻找引用类数据时首先在栈中找寻其指针，根据其指针在堆中找到引用类数据。     
> 图如下![](https://github.com/0ragdoll0/Front-end-Q-A/blob/master/pic/stackandheap.PNG)
