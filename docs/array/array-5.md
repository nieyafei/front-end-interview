# 找出数字数组中最大的元素（使用Math.max函数）

- ### 直接使用

```js
var ans = Math.max(1, 2, 3, 4, 5, 6);
console.log(ans); // 6
```

- ### 使用apply

```js
var a = [1, 2, 3, 6, 5, 4, 8];
var ans = Math.max.apply(null, a);
console.log(ans);  // 6
```
- ### 使用call+ES6

```js
var a = [1, 2, 3, 6, 5, 4, 8];
var ans = Math.max.call(null, ...a);
console.log(ans);  // 6
```

- ### eval+toString

```js
var a = [1, 2, 3, 6, 5, 4];
var ans = eval( 'Math.max(' + a.toString() + ')');
console.log(ans); // 6
```
- ### ES6

```js
let a = [1, 2, 3, 6, 5, 4];
let maxn = Math.max(...a);
console.log(maxn); // 6
```

**参考资料：**

[题目来源](http://www.cnblogs.com/zichi/p/4362292.html)
