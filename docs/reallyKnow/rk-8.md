# 警惕IEEE 754标准

```js
var two   = 0.2
var one   = 0.1
var eight = 0.8
var six   = 0.6
[two - one == one, eight - six == two]
```

?> `结果是`[true,false]

> JavaScript中采用`双精度浮点数格式`，即`IEEE 754标准`。在该格式下，有些数字无法表示出来，比如：`0.1 + 0.2 = 0.30000000000000004` ，这不是JavaScript的锅，所有采用该标准的语言都有这个问题，比如：Java、Python等。

**参考资料：**

[Double-precision floating-point format](https://en.wikipedia.org/wiki/Double-precision_floating-point_format)

[资料来源：点击测试](http://javascript-puzzlers.herokuapp.com/)

[参考文档](http://f2ex.cn/do-you-really-know-javascript/)