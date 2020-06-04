# 神鬼莫测之变量提升

```js
var name = 'World!';
(function () {
    if (typeof name === 'undefined') {
        var name = 'Jack';
        console.log('Goodbye ' + name);
    } else {
        console.log('Hello ' + name);
    }
})();
```

?> `答案：`Goodbye Jack


**参考资料：**

[资料来源：点击测试](http://javascript-puzzlers.herokuapp.com/)

[MDN: 变量提升](https://developer.mozilla.org/zh-CN/docs/Glossary/Hoisting)