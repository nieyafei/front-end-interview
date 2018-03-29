# 2、下面的代码将输出到控制台，为什么？

```js
(function(){
  var a = b = 3;
})();

console.log("a defined? " + (typeof a !== 'undefined'));
console.log("b defined? " + (typeof b !== 'undefined'));
```

?> `答案：`a defined? false /  b defined? true

### 解析：

首先要理解的一句话是在`立即执行函数体`里面的`var a = b = 3;`,对这个进行拆解一下
(`赋值过程从右到左`)

```js
b = 3;
var a = b;
```

- 变量`b`是一个全局变量
- 变量`a`在封闭的立即执行函数作用域下的局部变量

因此`typeof a` 是`undefined`, `typeof b`是`number`

**以上是在`非严格模式`下，如果在`严格模式（use strict）`下，声明`var a = b = 3`；将产生一个运行时错误的`ReferenceError: b is not defined`**

**参考资料：**

[原题来源](https://www.toptal.com/javascript/interview-questions)
