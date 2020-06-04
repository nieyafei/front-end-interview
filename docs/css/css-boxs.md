# 介绍一下box-sizing

> 设置CSS盒模型为标准模型或IE模型。标准模型的宽度只包括content，二IE模型包括border和padding

> box-sizing属性允许您以特定的方式定义匹配某个区域的特定元素。

box-sizing属性可以为三个值：

- `content-box`，默认值，只计算内容的宽度，border和padding不计算入width之内

> 尺寸计算公式：width = 内容的宽度，height = 内容的高度。宽度和高度都不包含内容的边框（border）和内边距（padding）。

- `border-box`，border和padding计算入宽度之内

> width = border + padding + 内容的  width，
height = border + padding + 内容的 height

- `inherit`，指定box-sizing属性的值，应该从父元素继承

**参考资料：**

[CSS3 box-sizing 属性](http://www.w3school.com.cn/cssref/pr_box-sizing.asp)

[MDN box-sizing](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-sizing)