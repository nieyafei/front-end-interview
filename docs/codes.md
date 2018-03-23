## JS判断字符串是否含有中文

```js
if (escape(str).indexOf("%u") > 0) { 
  //字符串 str 中含有汉字 
} 
```

## 检查给定参数是否为数组

`Array.isArray()`

```js
let isArray =(val)=> !!val && Array.isArray(val);
```

## 检查给定的参数是否为Boolean

```js
let isBoolean =(val)=> typeof val === 'boolean';
```

## 判断参数是否为数字

```js
let isNumber =(str)=> typeof str === 'number';
```

## 判断参数是否为字符串

```js
let isString =(str)=> typeof str === 'string';
```

## 判断参数是否为符号

```js
let isSymbol =(str)=> typeof str === 'symbol';
```

## 判断是否为函数

```js
let isFunction =(str)=> typeof str === 'function';
```
