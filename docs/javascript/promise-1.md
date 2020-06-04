# 代码块（阿里二面）

### 请回答打印的结果是多少？

```js
var p1=new Promise(resolve => {
    console.log(1)
    resolve(2)
})
var p2=new Promise(resolve => {
    console.log(3)
    resolve(p1)
})
p1.then(re => {
    console.log(re)    
})
p2.then(re => {
    console.log(re)
})

```

**参考资料：**
  
  [题目来源](https://segmentfault.com/q/1010000013721635?utm_source=feed-content)
