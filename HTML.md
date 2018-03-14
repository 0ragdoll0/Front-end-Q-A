1. Doctype作用？标准模式与兼容模式各有什么区别?**(文档标准，最高标准，向后兼容)**
>     (1)<!DOCTYPE>声明位于位于HTML文档中的第一行，处于 <html> 标签之前。告知浏览器的解析器用什么文档标准解析这个文档。DOCTYPE不存在或格式不正确会导致文档以兼容模式呈现。
>     (2)标准模式的排版和JS运作模式都是以该浏览器支持的最高标准运行。在兼容模式中，页面以宽松的向后兼容的方式显示,模拟老式浏览器的行为以防止站点无法工作。

2. HTML5 为什么只需要写\<!DOCTYPE HTML\>？
>     (1)HTML5 不基于SGML(Standard Generalized Markup Language,标准通用标记语言)，因此不需要对DTD(Document Type Definition,文档类型定义)进行引用，但是需要doctype来规范浏览器的行为（让浏览器按照它们应该的方式来运行）；
>     (2)HTML4.01基于SGML,所以需要对DTD进行引用，才能告知浏览器文档所使用的文档类型

3. 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？
>     (1)行内元素：span input select img a strong b 
>     (2)快级元素：div h p ul ol li dl dt dd
>     (3)空元素：meta link input img br hr

4. 页面导入样式时，使用link和@import有什么区别？**(RSS，加载顺序，兼容IE5)**
>     (1)link属于XHTML标签，除了加载CSS外，还能用于定义RSS(Really Simple Syndication,简易信息聚合), 定义rel连接属性等作用；而@import是CSS提供的，只能用于加载CSS;
>     (2)页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;
>     (3)import是CSS2.1 提出的，只在IE5以上才能被识别，而link是XHTML标签，无兼容问题;
>     (4)import规则一定要先于除了@charset的其他任何CSS规则
> @import在IE中容易破坏并行载入，下载顺序容易紊乱[高性能网站设计：不要使用@import](https://www.qianduan.net/high-performance-web-site-do-not-use-import/)

5. 浏览器内核的理解？
>     (1)渲染引擎：负责取得网页的内容（HTML、XML、图像等等）、整理讯息（例如加入CSS等），以及计算网页的显示方式，然后会输出至显示器或打印机。浏览器的内核的不同对于网页的语法解释会有不同，所以渲染的效果也不相同。所有网页浏览器、电子邮件客户端以及其它需要编辑、显示网络内容的应用程序都需要内核。
>     (2)JS引擎则：解析和执行javascript来实现网页的动态效果。

6. 常见的浏览器内核有哪些？
>     Trident内核：IE,MaxThon,TT,The World,360,搜狗浏览器等。[又称MSHTML]和W3C标准脱节。
>     Gecko内核：Netscape6及以上版本，FF,MozillaSuite/SeaMonkey等。优点就是功能强大、丰富，可以支持很多复杂网页效果和浏览器扩展接口，代价是消耗很多的资源，比如内存。
>     Presto内核：Opera7及以上。[Opera内核原为：Presto，现为：Blink;]被称为公认的浏览网页速度最快的内核，丢掉了一部分网页兼容性。
>     Webkit内核：Safari,Chrome等。   [ Chrome的：Blink（WebKit的分支）]网页浏览速度较快，容错性差
> [浏览器内核的解析和对比](http://www.cnblogs.com/fullhouse/archive/2011/12/19/2293455.html)

7. HTML语义化
>     (1)让页面内容结构更清晰，便于解析
>     (2)使阅读源码的人容易将网页分块（比起全是div的页面）
>     (3)在没有CSS的情况下以文档格式显示且容易阅读
>     (4)有利于搜索引擎优化(不同标签权重不同)

8. title与h1的区别、b与strong的区别、i与em的区别？(b、i都是表现（视觉）元素)
>     (1)title只是标题，没有明确意义。H1表示层次明确的标题，对页面信息的抓取也有很大的影响；
>     (2)strong语气加强，b强调内容
>     (3)em表示强调的文本，i内容展示为斜体


9. 实现不使用 border 画出1px高的线，在不同浏览器的标准模式与怪异模式下都能保持一致的效果。
```
<div style="height:1px;overflow:hidden;background:red"></div>
```
