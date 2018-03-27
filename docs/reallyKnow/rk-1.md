# 当parseInt遇到map

```js
["1", "2", "3"].map(parseInt)
```

**输出打印结果**

> 结果：[1, NaN, NaN]

### **解析：**

- #### map

?> callback(currentValue, index, array)

> `currentValue`: 数组中正在处理的当前元素

> `index`:  数组中正在处理的当前元素的索引

> `array`: map 方法被调用的数组

- #### parseInt

?> 语法：**parseInt(string, radix)  **

> **string解析的字符串，若不是字符串则转换为字符串**

> **radix是一个介于2-36之间的整数，表示字符串的`基数`,当未指定基数时或者基数为`0`，不同的实现会产生不同的结果，通常将值默认为10**

?> 如果被解析参数的第一个字符无法被转化成数值类型，则返回 NaN

此题解析之后：

- `parseInt("1",0)`, 以10进制转换，返回1

- `parseInt("2",1)`, 基数非法，返回`NaN`

- `parseInt("3",2)`, 以二进制转换，第一个参数非法，返回`NaN`


**参考资料：**

- [map-MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Map)

- [parseInt-MDN](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/parseInt)

