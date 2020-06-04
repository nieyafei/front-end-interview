# 6、两个函数运行结果一样吗？为什么？

```js
// 函数1
function foo1()
{
  return {
      bar: "hello"
  };
}

// 函数2
function foo2()
{
  return
  {
      bar: "hello"
  };
}

console.log(foo1());
console.log(foo2());
```

> `结果：` 不会一样

> Object {bar: "hello"}

> undefined

### 解析：

**由于 Javascript 的`;`插入机制决定的，如果某行代码，return 关键词后没有任何东西了，将会自动插入一个`;`,因此在`foo2函数中`会是`return;`,后面的则不会继续执行了，因此返回`undefined`**

**参考资料：**

[原题来源](https://www.toptal.com/javascript/interview-questions)