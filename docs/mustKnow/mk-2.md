# 下面的代码将输出到控制台，为什么？<i class='iconS'></i><i class='iconS'></i><i class='iconS'></i>

```js
var myObject = {
    foo: "bar",
    func: function() {
        var self = this;
        console.log("outer func:  this.foo = " + this.foo);
        console.log("outer func:  self.foo = " + self.foo);
        (function() {
            console.log("inner func:  this.foo = " + this.foo);
            console.log("inner func:  self.foo = " + self.foo);
        }());
    }
};
myObject.func();
```

> `答案：`

> outer func:  this.foo = bar

> outer func:  self.foo = bar

> inner func:  this.foo = undefined

> inner func:  self.foo = bar

### 解析

在外部函数func中的，`this`指向的对象是`myObject`,因此`self`也指向`myObject`

在内部函数中， `this` 不再指向 `myObject`。其结果是，`this.foo` 没有在内部函数中被定义，相反，指向到本地的变量`self` 保持在范围内，并且可以访问。 （在ECMA 5之前，在内部函数中的this 将指向全局的 window 对象；反之，因为作为ECMA 5，内部函数中的功能this 是未定义的。）

**参考资料：**

[原题来源](https://www.toptal.com/javascript/interview-questions)

