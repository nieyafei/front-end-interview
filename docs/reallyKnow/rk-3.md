# 对于愤怒的reduce

```js
[ [3,2,1].reduce(Math.pow), [].reduce(Math.pow) ]
```

?> an error

### 解析：

?> `arr.reduce(callback[, initialValue])` 方法对累加器和数组中的每个元素（从左到右）应用一个函数，将其减少为单个值

?> `Math.pow(base, exponent)` 函数返回基数（`base`）的指数（`exponent`）次幂。

**对于`[3,2,1].reduce(Math.pow)`**

```js
Math.pow(3,2);// 9
Math.pow(9,1);// 9
```

**对于[].reduce(Math.pow)**

> `Uncaught TypeError: Reduce of empty array with no initial value`

**参考资料：**

[MDN: reduce()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

[MDN: Math.pow()](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/pow)

[资料来源：点击测试](http://javascript-puzzlers.herokuapp.com/)

