# 头痛的优先级

```js
var val = 'smtg';
console.log('Value is ' + (val === 'smtg') ? 'Something' : 'Nothing');
```

?> `结果是` Something

### 解析：

**运算符`+`优先于运算符`?`**

因此题目就会变为
```
('Value is ' + (val === 'smtg')) ? 'Something' : 'Nothing'
等于
true ? 'Something' : 'Nothing'
```
**参考资料：**

[MDN: 表达式和运算符](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_Operators#%E8%BF%90%E7%AE%97%E7%AC%A6%E4%BC%98%E5%85%88%E7%BA%A7(Operator_precedence))
