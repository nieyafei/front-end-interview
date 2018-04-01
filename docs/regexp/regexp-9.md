# 匹配ip地址

```js
var ipStr = "255.254.1.1";
var reg = /(([01]?\d\d?|2[0-4]\d|25[0-5])\.){3}([01]?\d\d?|2[0-4]\d|25[0-5])/g;

// 匹配
console.log(str.match(reg));
```