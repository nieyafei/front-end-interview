# 对于this对象的理解

?>`谁调用的方法this就是指向谁`

首先要理解`调用位置`,调用位置就是函数在代码中被调用的位置（而不是声明的位置）。

具体详情，我建议看一下`《你不知道的js》`这本书

|调用形式|this指向|
|:-----:|:-----:|
|普通函数|window|
|构造函数|实例化后的对象|
|对象的方法|该对象|
|DOM节点|该节点对象|
|call或者apply|传入的第一个参数|

**参考资料：**

[MDN: this](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/this)

[深入理解this对象](https://blog.csdn.net/woshinannan741/article/details/51146889)

[如何理解 JavaScript 中的 this 关键字？](https://www.zhihu.com/question/19636194)

[JavaScript中的对象查找](http://www.otakustay.com/object-lookup-in-javascript/)
