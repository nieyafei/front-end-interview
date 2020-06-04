# 过滤器魔法

```js
var ary = [0,1,2];
ary[10] = 10;
ary.filter(function(x) { return x === undefined;});
```

?> `结果是` []

### 解析：

> **`filter()` 方法创建一个新数组, 其包含通过所提供函数实现的测试的所有元素**

> filter 为数组中的每个元素调用一次 callback 函数，并利用所有使得 callback 返回 true 或 等价于 true 的值 的元素创建一个新数组。callback 只会在已经赋值的索引上被调用，对于那些已经被删除或者从未被赋值的索引不会被调用。那些没有通过 callback 测试的元素会被跳过，不会被包含在新数组中。

**参考资料：**

[MDN: Array.prototype.filter()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

[资料来源：点击测试](http://javascript-puzzlers.herokuapp.com/)

[参考文档](http://f2ex.cn/do-you-really-know-javascript/)