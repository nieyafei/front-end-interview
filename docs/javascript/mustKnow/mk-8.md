# 9、写一个方法 isInterger(x)，可以用来判断一个变量是否是整数

?> Discuss possible ways to write a function isInteger(x) that determines if x is an integer.

> `ES6` 中自带了 `Number.isInteger()` 方法

**针对ES5的函数**

```js
function isInteger(x) { 
  return parseInt(x, 10) === x; 
}
```

**参考资料：**

[Number.isInteger()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number/isInteger)