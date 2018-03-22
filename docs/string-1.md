# 请给字符串都添加上原型方法 spacify，可以让一个字符串的每个字母都多出一个空格的间隔

`"ScriptOJ".spacify() // => "S c r i p t O J"`

### 答案解析：

```js
String.prototype.spacify = function () {
  return this.split('').join(' ')
}
```

**参考资料：**

[本题来源](http://blog.sourcing.io/interview-questions)