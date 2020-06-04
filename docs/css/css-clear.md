# 清除浮动的方法

- ### 父级div定义 高度

> 给父级DIV定义固定高度（height），能解决父级DIV 无法获取高度得问题。 优点：代码简洁 缺点：高度被固定死了，是适合内容固定不变的模块。`（不推荐使用）`

- ### 使用空元素

> `<div style="clear:both;"></div>`<br>
添加一对空的DIV标签，利用css的clear:both属性清除浮动，让父级DIV能够获取高度。 优点：浏览器支持好 缺点：多出了很多空的DIV标签，如果页面中浮动模块多的话，就会出现很多的空置DIV了，这样感觉视乎不是太令人满意。`（不推荐使用）`

- ### 父级div浮动起来

> 可以初步解决当前的浮动问题,但是又会产生新的浮动问题。`（不推荐使用）`

- ### 父级div定义 display:table

> 将div属性强制变成表格 优点：不解 缺点：会产生新的未知问题。`（不推荐使用）`

- ### 父元素设置 overflow：hidden、auto

> 这个方法的关键在于触发了BFC。在IE6中还需要触发 hasLayout（zoom：1） 优点：代码简介，不存在结构和语义化问题 缺点：无法显示需要溢出的元素`（亦不太推荐使用）`

- ### 父级div定义伪类:after 和 zoom

> **IE8以上和非IE浏览器才支持:after，原理和方法`空元素`有点类似，zoom(IE转有属性)可解决ie6,ie7浮动问题 优点：结构和语义化完全正确,代码量也适中，可重复利用率（建议定义公共类） 缺点：代码不是非常简洁`（极力推荐使用）`**

```
.clearfix:after{
    content:'.';
    display:block;
    height:0;
    clear:both;
    visibility: hidden;
}
.clearfix {*zoom:1;}
```

**参考资料：**

[题目来源和答案](https://juejin.im/post/5a954add6fb9a06348538c0d)
