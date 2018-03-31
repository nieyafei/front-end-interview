# 经典关于this面试知识点题目

```js
var a=10;
var foo={
  a:20,
  bar:function(){
      var a=30;
      return this.a;
    }
}
foo.bar()
(foo.bar)()
(foo.bar=foo.bar)()
(foo.bar,foo.bar)()
```

**结果：**

```js
20
20
10
10
```

### 解析：

?> `foo.bar()` 的this指向`foo`,因此是20

?> `(foo.bar)()`: `foo.bar`是匿名函数，调用函数`()`,this指向匿名函数，这个匿名函数仅限于foo里面的全局变量使用，this.a就是foo里面的全局变量a，因此等价于`foo.bar()`

?> `(foo.bar=foo.bar)()`: 从右向左进行赋值foo.bar被重新赋值一个函数，然后再执行这个匿名函数，但是此时的函数被赋值之后，`this`指向了全局变量`window`,因此是10

?> `(foo.bar,foo.bar)()`: 逗号运算符，执行左边的`foo.bar`的函数，此时的this指向`window`,因此是10


**参考资料：**

[逗号运算符](https://www.zhihu.com/question/27620371)
