# 字符串陷阱

```js
function showCase(value) {
    switch(value) {
        case 'A':
            console.log('Case A');
            break;
        case 'B':
            console.log('Case B');
            break;
        case undefined:
            console.log('undefined');
            break;
        default:
            console.log('Do not know!');
    }
}
showCase(new String('A'));
```

?> `结果是` Do not know!

```js
function showCase2(value) {
    switch(value) {
    case 'A':
        console.log('Case A');
        break;
    case 'B':
        console.log('Case B');
        break;
    case undefined:
        console.log('undefined');
        break;
    default:
        console.log('Do not know!');
    }
}
showCase2(String('A'));
```

?> `结果是` Case A

> 在 `switch` 内部使用严格相等 `===` 进行判断，并且 `new String("A")` 返回的是一个对象，而 `String("A")` 则是直接返回字符串 `"A"`。

**字符串字面量 (通过单引号或双引号定义) 和 直接调用 String 方法(没有通过 new 生成字符串对象实例)的字符串都是基本字符串。JavaScript会自动将基本字符串转换为字符串对象，只有将基本字符串转化为字符串对象之后才可以使用字符串对象的方法。当基本字符串需要调用一个字符串对象才有的方法或者查询值的时候(基本字符串是没有这些方法的)，JavaScript 会自动将基本字符串转化为字符串对象并且调用相应的方法或者执行查询。**

**参考资料：**

[基本字符串和字符串对象的区别](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String)

[资料来源：点击测试](http://javascript-puzzlers.herokuapp.com/)

[参考文档](http://f2ex.cn/do-you-really-know-javascript/)