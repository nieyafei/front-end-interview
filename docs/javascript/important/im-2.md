# 涉及同步、异步、作用域、闭包四连问

## 基础代码块

```js
for (var i = 0; i < 5; i++) {
    setTimeout(function() {
        console.log(i);
    }, 1000);
}

console.log(i);
```

?> `答案是`  5  5  5  5  5  5

## 追问：闭包

?> **期望代码的输出变成：5 -> 0,1,2,3,4，该怎么改造代码**

- 闭包

```js
for (var i = 0; i < 5; i++) {
    (function(j) {  // j = i
        setTimeout(function() {
            console.log(j);
        }, 1000);
    })(i);
}

console.log(i);
```
- 按值传递

```js
var output = function (i) {
    setTimeout(function() {
        console.log(i);
    }, 1000);
};

for (var i = 0; i < 5; i++) {
    output(i);  // 这里传过去的 i 值被复制了
}

console.log(i);
```

- ES6的let

```js
for (let i = 0; i < 5; i++) {
    setTimeout(function() {
        console.log(new Date, i);
    }, 1000);
}

console.log(new Date, i);
```

## 追问：ES6

?> **如果期望代码的输出变成 0 -> 1 -> 2 -> 3 -> 4 -> 5，并且要求原有的代码块中的循环和两处 console.log 不变，该怎么改造代码？**

```js
const tasks = []; // 这里存放异步操作的 Promise
const output = (i) => new Promise((resolve) => {
    setTimeout(() => {
        console.log(new Date, i);
        resolve();
    }, 1000 * i);
});

// 生成全部的异步操作
for (var i = 0; i < 5; i++) {
    tasks.push(output(i));
}

// 异步操作完成之后，输出最后的 i
Promise.all(tasks).then(() => {
    setTimeout(() => {
        console.log(new Date, i);
    }, 1000);
});
```

## 追问：ES7

?> **如何使用 ES7 中的 `async` `await` 特性来让这段代码变的更简洁？你是否能够根据自己目前掌握的知识给出答案？**

```js
const sleep = (timeountMS) => new Promise((resolve) => {
    setTimeout(resolve, timeountMS);
});

(async () => {  // 声明即执行的 async 函数表达式
    for (var i = 0; i < 5; i++) {
        await sleep(1000);
        console.log(new Date, i);
    }

    await sleep(1000);
    console.log(new Date, i);
})();
```


**参考资料：**

[题目来源](https://www.nowcoder.com/discuss/22377)