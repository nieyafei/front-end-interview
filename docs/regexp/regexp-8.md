# 邮政编码的验证（开头不能为0，共6位）

```js
function isPostalCode(str){
    return /^[1-9][0-9]{5}$/.test(str)
}
```

**参考资料：**

[正则表达式](http://www.runoob.com/regexp/regexp-syntax.html)

[MDN: 正则表达式](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions)