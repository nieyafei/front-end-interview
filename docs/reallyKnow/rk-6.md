# 死循环陷阱

```js
var END = Math.pow(2, 53);
var START = END - 100;
var count = 0;
for (var i = START; i <= END; i++) {
    count++;
}
console.log(count);
```

?> 这个会陷入一个死循环，`2^53`是最大的值，因此`2^53+1` 等于 `2^53`

**参考资料：**

[资料来源：点击测试](http://javascript-puzzlers.herokuapp.com/)