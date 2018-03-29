# 10、在下面的代码中，数字 1-4 会以什么顺序输出？为什么会这样输出？

```js
(function() {
    console.log(1); 
    setTimeout(function(){console.log(2)}, 1000); 
    setTimeout(function(){console.log(3)}, 0); 
    console.log(4);
})();
```

> `结果：` 1  4  3  2

**JavaScript引擎是单线程运行的,浏览器无论在什么时候都只且只有一个线程在运行JavaScript程序**

**setTimeout和setInterval是伪线程**

> 立即执行函数里面的`1  4`会优先执行，setTimeout则是会进入异步队列等待执行，因为有时间的延迟，因此`3`先执行，`2`后执行

具体详情看参考资料详解

**参考资料：**

[JavaScript 运行机制详解：再谈Event Loop](http://www.ruanyifeng.com/blog/2014/10/event-loop.html)

[从setTimeout谈JavaScript运行机制](https://www.cnblogs.com/zichi/p/4604053.html)