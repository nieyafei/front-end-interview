# display:inline-block 什么时候会显示间隙？

?> 该元素生成一个块状盒，该块状盒随着周围内容流动，如同它是一个单独的行内盒子（表现更像是一个被替换的元素）

> 1、有空格时候会有间隙 解决：移除空格

> 2、`margin`正值的时候 解决：`margin`使用负值

> 3、使用`font-size`时候 解决：`font-size:0`、`letter-spacing`、`word-spacing`


**参考资料：**

[MDN: display](https://developer.mozilla.org/zh-CN/docs/Web/CSS/display)
