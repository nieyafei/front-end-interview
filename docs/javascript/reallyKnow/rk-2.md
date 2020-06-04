# 关于null

```js
[typeof null, null instanceof Object]
```

**输出打印结果：**

> 结果： ["object", false]

###  **解析：**

- ### typeof

?> `typeof`操作符返回一个字符串，表示未经计算的操作数的类型

|类型|结果|
|:------:|:------:|
| `Undefined` | `"undefined"` |
| `Null` | `"object"` |
| `Boolean` | `"boolean"` |
| `Number` | `"number"` |
| `String` | `"string"` |
| `Symbol` | `"symbol"` |
| `函数对象` | `"function"` |
| `任何其他对象` | `"object"` |


```js
typeof null === 'object';// 从最开始的时候javascript就是这样
```
JavaScript 中的值是由一个表示类型的标签和实际数据值表示的。对象的类型标签是 0。由于 null 代表的是空指针（大多数平台下值为 0x00），因此，null的类型标签也成为了 0，typeof null就错误的返回了"object"。这算一个bug,但是被拒绝修复，因为影响的web系统太多

- ### instanceof

?> `instanceof` 运算符用来测试一个对象在其原型链中是否存在一个构造函数的 prototype 属性

> `null`不是以`Object`原型创建，因此返回`false`

**参考资料：**

[MDN：typeof](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/typeof)

[MDN：instanceof](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/instanceof)