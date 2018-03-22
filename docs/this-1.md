# 代码块☆☆☆

```js

var myObject = {
  foo: "bar",
  func: function() {
    var self = this;
    console.log("outer func: this.foo = " + this.foo);
    console.log("outer func: self.foo = " + self.foo);
    (function() {
      console.log("inner func: this.foo = " + this.foo);
      console.log("inner func: self.foo = " + self.foo);
    })()
  }
}
myObject.func();

```

`输出结果如下：`

```js
outer func: this.foo = bar
outer func: self.foo = bar
inner func: this.foo = undefined
inner func: self.foo = bar

```

在外部函数func中的，this指向的对象是myObject,因此self也指向myObject

在内部函数中， this 不再指向 myObject。其结果是，this.foo 没有在内部函数中被定义，相反，指向到本地的变量self 保持在范围内，并且可以访问。 （在ECMA 5之前，在内部函数中的this 将指向全局的 window 对象；反之，因为作为ECMA 5，内部函数中的功能this 是未定义的。）