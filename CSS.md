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
