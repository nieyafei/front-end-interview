# setTimeout面试连击 

## 第一击

```js
for (var i = 0; i < 5; i++) {
  console.log(i);
}
```

> `答案：` 0  1  2  3  4


## 第二击

```js
for (var i = 0; i < 5; i++) {
  setTimeout(function() {
    console.log(i);
  }, 1000 * i);
}
```

> `答案：` 5   5   5   5  5

## 第三击

**怎么修改输出0  1  2  3  4**

```js
# 闭包模式   或者Es6的`let`
for (var i = 0; i < 5; i++) {
  (function(i) {
    setTimeout(function() {
      console.log(i);
    }, i * 1000);
  })(i);
}
```


## 第四击

```js
for (var i = 0; i < 5; i++) {
  (function() {
    setTimeout(function() {
      console.log(i);
    }, i * 1000);
  })(i);
}
```

> `答案：` 5  5   5   5   5


## 第五击

```js

for (var i = 0; i < 5; i++) {
  setTimeout((function(i) {
    console.log(i);
  })(i), i * 1000);
}

```

> `答案：` 0  1  2   3   4

## 第六击

**运行机制**

```js
setTimeout(function() {
  console.log(1)
}, 0);
new Promise(function executor(resolve) {
  console.log(2);
  for( var i=0 ; i<10000 ; i++ ) {
    i == 9999 && resolve();
  }
  console.log(3);
}).then(function() {
  console.log(4);
});
console.log(5);
```

**setTimeout**


**参考资料：**

[题目来源](https://zhuanlan.zhihu.com/p/25407758)
