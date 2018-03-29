# 为什么要用立即执行函数表达式（Immediately-Invoked Function Expression）？

?> What is the significance of, and reason for, wrapping the entire content of a JavaScript source file in a function block?

> IIFE: Immediately Invoked Function Expression，意为立即调用的函数表达式，也就是说，声明函数的同时立即调用这个函数

正常来说函数声明和函数调用

```js
function foo(){console.log('CODEHTML')} // 声明
foo();// 调用
```

如果使用IIFE形式的函数调用(`匿名函数表达式`)

```js
(function(){
  console.log('CODEHTML');
})()
```

`IIFE`还有一种用途就是`倒置代码的运行顺序`

```js
var a = 2;
(function(def){
  def(window);
})(function def(global){
  var a = 3;
  console.log(a);
  console.log(global.a);
})
// 来自《你不知道的js》
```

**参考资料：**

[原题来源](https://www.toptal.com/javascript/interview-questions)
