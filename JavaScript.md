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
> ![](https://github.com/0ragdoll0/Front-end-Q-A/blob/master/pic/stackandheap.PNG)

5. js中this值
> 1. 函数（全局函数/对象中定义的方法）中this代表实际调用此函数的对象（window/实例）   
> 2. 构造函数中有this，通过new，this代表新建的对象实例    
> 3. settimeout中this代表windows对象（即使是实例对象调用时），可通过bind改变

6.settimeout
> 1. 运行机制：将指定的代码移出本次执行，等到下一轮Event Loop时，再检查是否到了指定时间。如果到了，就执行对应的代码；如果不到，就等到再下一轮Event Loop时重新判断。这意味着，setTimeout指定的代码，必须等到本次执行的所有代码都执行完，才会执行。   
> 2. settimeout(f,0):让f在现有的任务（脚本的同步任务和“任务队列”中已有的事件）一结束就立刻执行.->可用于调整事件处理顺序。     
> 详解：[你所不知道的setTimeout](https://jeffjade.com/2016/01/10/2016-01-10-javacript-setTimeout/)
