# setTimeout最小间隔4ms的问题

```js
setTimeout(()=>{console.log(5)},5)
setTimeout(()=>{console.log(4)},4)
setTimeout(()=>{console.log(3)},3)
setTimeout(()=>{console.log(2)},2)
setTimeout(()=>{console.log(1)},1)
setTimeout(()=>{console.log(0)},0)
```

### 不同的浏览器打印结果不一样？

- Chrome+Safari(mac)

> 1  0  2  3  4  5

- Firefox(mac)

> 0  1  2  3  4  5 

**参考资料：**

[问题来源](https://segmentfault.com/q/1010000014975261)