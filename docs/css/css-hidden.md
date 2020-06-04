# CSS隐藏元素的几种方式及区别

### display:none

> - 元素在页面上将彻底消失，元素本来占有的空间就会被其他元素占有，也就是说它会导致浏览器的重排和重绘。

> - 不会触发其点击事件

### visibility:hidden

> - 和display:none的区别在于，元素在页面消失后，其占据的空间依旧会保留着，所以它只会导致浏览器重绘而不会重排。

> - 无法触发其点击事件

> - 适用于那些元素隐藏后不希望页面布局会发生变化的场景

### opacity:0

> - 将元素的透明度设置为0后，在我们用户眼中，元素也是隐藏的，这算是一种隐藏元素的方法。

> - 和visibility:hidden的一个共同点是元素隐藏后依旧占据着空间，但我们都知道，设置透明度为0后，元素只是隐身了，它依旧存在页面中。

> - 可以触发点击事件

### position

> - 将元素移出可视区域，ps: left:-9999px

### clip-path

> - 通过剪裁实现，`此功能某些浏览器尚在开发中`

### 设置height，width等盒模型属性为0

> - 简单说就是将元素的margin，border，padding，height和width等影响元素盒模型的属性设置成0，如果元素内有子元素或内容，还应该设置其overflow:hidden来隐藏其子元素，这算是一种奇技淫巧

> - 如果元素设置了border，padding等属性不为0，很显然，页面上还是能看到这个元素的，触发元素的点击事件完全没有问题。如果全部属性都设置为0，很显然，这个元素相当于消失了，即无法触发点击事件

> - 这种方式既不实用，也可能存在着着一些问题。但平时我们用到的一些页面效果可能就是采用这种方式来完成的，比如jquery的slideUp动画，它就是设置元素的overflow:hidden后，接着通过定时器，不断地设置元素的height，margin-top，margin-bottom，border-top，border-bottom，padding-top，padding-bottom为0，从而达到slideUp的效果


**参考资料：**

[题目和答案来源](https://juejin.im/post/5a954add6fb9a06348538c0d)

[MDN: clip-path](https://developer.mozilla.org/zh-CN/docs/Web/CSS/clip-path)