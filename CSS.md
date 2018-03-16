1. 介绍一下标准的CSS的盒子模型？低版本IE的盒子模型有什么不同的？
>     盒模型：content、padding、border、margin
>     标准盒模型的width只包括content，低版本IE（5.5）width包括了content、padding、border
>     可设置box-sizing:content-box或border-box来选择标准盒模型或者IE盒模型

2. CSS选择符（**9**）？哪些属性可以继承?
- id选择器（权重：100）
- 类选择器（权重：10）
- 标签选择器（权重：1）
- 相邻选择器（+）
- 子选择器（>）(注意和后代选择器区分)
- 后代选择器
- 通配符选择器（*）
- 属性选择器（a[rel = "external"]）
- 伪类选择器（a:hover, li:nth-child）
>     可继承：font-size font-family color,UL LI DL DD DT
>     不可继承（盒子模型中属性）:width height padding border margin

3. CSS优先级算法如何计算？
>     优先级：内联>内部>外部
>     计算权重：1000,100,10,1，权重相同后载入优先
>     !important优先级最高
>     创作者高于浏览者

4. 居中问题
>     水平居中
>     垂直居中
>     水平垂直居中
具体见笔记[定位和居中](https://github.com/0ragdoll0/ife/blob/master/w_task4/%E5%AE%9A%E4%BD%8D%E5%92%8C%E5%B1%85%E4%B8%AD%E7%AC%94%E8%AE%B0.docx)

5. display有哪些值？说明他们的作用。
>     none 元素不被显示
>     block 块级元素，可设置宽高，换行显示
>     inline 行内元素，行内显示
>     inline-block 可设置宽高，行内显示
>     table 作为块级表格来显示（类似 <table>），表格前后带有换行符。
>     list-item 作为列表显示
>     inherit
 
6. display:inline-block 什么时候会显示间隙(li之间)
> 元素之间的空白（回车、空格）也算字符。解决方法：删除空白、将父元素font-size设置为0、margin设置负值

7. position的值及其定位原点是？
>     relative 相对于其正常位置
>     absolute 相对于其第一个不是static的父元素
>     fixed 相对浏览器窗口
>     static 正常位置
>     inherit

8. 纯CSS创建一个三角形
>   #demo {
    width: 0;
    height: 0;
    border-width: 20px;
    border-style: solid;
    border-color: transparent transparent red transparent;
  }

