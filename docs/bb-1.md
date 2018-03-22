# 代码片段输出什么结果 <i class='iconS'></i><i class='iconS'></i>

```js
function fn1(){
  for(var i=0;i<4;i++){
    var tc=setTimeout(function(i){
      console.log(i);
      clearTimeout(tc)
    },10,i);
  }
}
function fn2(){
  for(var i=0;i<4;i++){
    var tc=setInterval(function(i,tc){
      console.log(i);
      clearInterval(tc)
    },10,i,tc);
  }
}
fn1();
fn2();

```

> `fn1()`：**结果是 0    1    2**

> `fn2()`: **结果是 0    1    2     3......Infinite**

**参考资料：**

[题目来源](https://zhuanlan.zhihu.com/p/25514220)