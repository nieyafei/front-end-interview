# 素数因子: 如何求出一个数的所有素数因子？

> A: 执行一个while循环。开始除以2，如果不能整除，记录这个除数，直到完成。

```js
function primeFactors(n){
  var factors = [], 
      divisor = 2;
  while(n>2){
    if(n % divisor == 0){
       factors.push(divisor); 
       n= n/ divisor;
    }else{
      divisor++;
    }     
  }
  return factors;
}

primeFactors(69); //  = [3, 23]
```

- **问：运行时间复杂度是多少？ 你能做得更好吗？**

> **答：`O(n)`。可以将除数从3开始，累加2。因为，如果一个数被任何偶数整除，它将被2整除。因此，你不需要除以偶数。此外，你不会有一个大于其价值一半的因素。如果你想让它变得复杂，那就用第一题的补充概念吧。**


**参考资料**

[素数](https://baike.baidu.com/item/%E8%B4%A8%E6%95%B0/263515?fr=aladdin)

[JS: Interview Algorithm](http://thatjsdude.com/interview/js1.html)

[翻译：JS: Interview Algorithm](https://www.liayal.com/article/5ac46c20a6cf4e67bc05c9f4#%E6%96%B9%E6%B3%952)