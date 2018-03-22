# 数组去重

**题目：编写一个函数 unique(arr)，返回一个去除数组内重复的元素的数组。**

> unique([0, 1, 2, 2, 3, 3, 4, 5]) // => [0, 1, 2, 3, 4, 5]

> unique([0, 1, '1', '1', 2]) // => [0, 1, '1', 2]

### 答案解析：

```js
const unique = (arr) => [...new Set(arr)]
```

**set是Es6的数据结构**

**参考资料：**

[ECMAScript 6：Set 和 Map 数据结构](http://es6.ruanyifeng.com/#docs/set-map)