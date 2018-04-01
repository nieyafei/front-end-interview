# 检测人民币金额，两位小数

```js
var money = "10029233.34"
var reg = /^(([1-9]\d*)|0)(\.\d{2})?$/;

// 检测
reg.test(money);

// true  和   false
```