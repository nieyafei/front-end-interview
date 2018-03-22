## JS判断字符串是否含有中文

```js
if (escape(str).indexOf("%u") > 0) { 
  //字符串 str 中含有汉字 
} 
```