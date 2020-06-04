# 验证一个数是否是素数

```js
function isPrime(num){
    if (num === 2 || num === 3) {
        return true;
    };
    if (num % 2 === 0) {
        return false;
    };
    let divisor = 3,limit = Math.sqrt(num);
    while(limit >= divisor){
        if (num % divisor === 0) {
            return false;
        }
        else {
            divisor += 2;
        }
    }
    return true;
}
console.log(isPrime(30));  // false
```

**说明：**
> 必须在原数组上操作，不能拷贝额外的数组。
> 尽量减少操作次数。

点击来源题目能看到各路答案

**题目来源：**

[来源链接](https://mp.weixin.qq.com/s/VjCEqQCyLxlmaxFe1TWjnQ)
