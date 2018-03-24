# 如何判断一个变量是否为数组？<i class='iconS'></i><i class='iconS'></i>

### Object.prototype.toString

```js
var list = [1,2,3];
Object.prototype.toString.call(list);
```

### Array.isArray()

> Array.isArray() 用于确定传递的值是否是一个 Array

```js
var list = [1,2,3];
Array.isArray(list);
```

**参考资料：**

[Array.isArray()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/isArray)