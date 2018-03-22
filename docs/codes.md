## JS判断字符串是否含有中文

```js
if (escape(str).indexOf("%u") > 0) { 
  //字符串 str 中含有汉字 
} 
```

## 检查给定参数是否为数组

`Array.isArray()`

```
let isArray =(val)=> !!val && Array.isArray(val);
```

## 检查给定的参数是否为本机布尔元素

```
let isBoolean =(val)=> typeof val === 'boolean'
```
