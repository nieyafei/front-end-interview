# NaN 是什么？typeof 的结果是？如果判断一个变量的值是 NaN？

?> What is NaN? What is its type? How can you reliably test if a value is equal to NaN?

`NaN` 是一个全局对象的属性, `NaN` 是 'not a number' 的缩写, 虽然`不是一个数字`, 但是`typeof`的值是`number`

```js
typeof NaN;// number
```

> 等号运算符（== 和 ===） 不能被用来判断一个值是否是 NaN。必须使用 `Number.isNaN()` 或 `isNaN()` 函数

```js
NaN === NaN;        // false
Number.NaN === NaN; // false
isNaN(NaN);         // true
isNaN(Number.NaN);  // true
```

**参考资料：**

[原题来源](https://www.toptal.com/javascript/interview-questions)

[MDN: NaN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/NaN)