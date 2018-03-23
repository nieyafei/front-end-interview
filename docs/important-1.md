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



## 第四击


## 第五击




**参考资料：**

[题目来源](https://zhuanlan.zhihu.com/p/25407758)
