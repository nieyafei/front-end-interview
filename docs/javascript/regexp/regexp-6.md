# 对连字符串转换为驼峰命名法

### 要求：

> 比如字符串`get-element-by-id`,转换成`getElementById`

```js
function hump(str){
    return str.replace(/-(\w)/g,function($0,$1){
        return $1.toUpperCase();
    })
}
```

```js
function hump(str){
    return str.replace(/-(\w)/g,function(x){
        return x.slice(1).toUpperCase();
    })
}
```

**参考资料：**

[MDN: 正则表达式](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Guide/Regular_Expressions)