# 对BFC相关知识的了解

> **BFC(Block formatting context)直译为"块级格式化上下文"。它是一个独立的渲染区域，只有 Block-level box 参 与， 它规定了内部的 Block-level Box 如何布局，并且与这个区域外部毫不相干。**

### BFC布局规则：

> 内部的Box会在垂直方向，一个接一个地放置。

> Box垂直方向的距离由margin决定。属于同一个BFC的两个相邻Box的margin会发生重叠

> 每个元素的margin box的左边， 与包含块border box的左边相接触(对于从左往右的格式化，否则相反)。即使存在浮动也是如此。

> BFC的区域不会与float box重叠。

> BFC就是页面上的一个隔离的独立容器，容器里面的子元素不会影响到外面的元素。反之也如此。

> 计算BFC的高度时，浮动元素也参与计算


### 哪些元素会生成BFC?

> 根元素

> float属性不为none

> position为absolute或fixed

> display为inline-block, table-cell, table-caption, flex, inline-flex

> overflow不为visible

**参考资料：**

[理解CSS布局和BFC](https://www.w3cplus.com/css/understanding-css-layout-block-formatting-context.html)

[BFC 神奇背后的原理](http://www.cnblogs.com/lhb25/p/inside-block-formatting-ontext.html)