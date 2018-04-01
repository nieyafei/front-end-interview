# 判断是否符合 USD 格式

### 要求

> 给定字符串 str，检查其是否符合美元书写格式 

> 1、以 `$` 开始 

> 2、整数部分，从个位起，满 3 个数字用 , 分隔 

> 3、如果为小数，则小数部分长度为 2 

> 4、正确的格式如：$1,023,032.03 或者 $2.03，错误的格式如：$3,432,12.12 或者 $34,344.3

```js
function isUSD(str) {
   return /^\$\d{1,3}(,\d{3})*(\.\d{2})?$/.test(str);
}
```

**参考资料：**

[正则表达式](http://www.runoob.com/regexp/regexp-syntax.html)

[MDN: 正则表达式](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions)