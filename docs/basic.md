# 使用 typeof bar === "object" 来确定 bar 是否是对象的潜在陷阱是什么？如何避免这个陷阱？☆☆☆

### 知识点

`typeof`是检测给定的变量的数据类型
`"undefined"`--如果这个值未定义
`"boolean"`--如果这个值是布尔值
`"string"`--如果这个值是字符串
`"number"`--如果这个值是数值
`"object"`--如果这个值是对象或者null
`"function"`--如果这个值是函数

`typeof bar === "object"`用来检测是否为对象的方法，就像`typeof bar === "number"`

```
let bar = {a:1,b:2};
console.log(typeof bar === "object");// true
```
从知识点我们可以知道，判断object的时候，有可能是null,因特殊值`null`会被认为空的对象引用
```
let bar = null;
console.log(typeof bar === "object");// true
```
因此我们需要首先判断是否为空
```
let bar = null,a = {id:1},c = {},b;
console.log(bar !== null && typeof bar === "object");// false
console.log(a !== null && typeof a === "object");// true
console.log(c !== null && typeof c === "object");// true
console.log(b !== null && typeof b === "object");// false
```
那么如果`bar`变量是个Array呢？
```
let bar = [];
console.log(bar !== null && typeof bar === "object");// true

# 因此需要判断一下是否为数组
let bar = [];
console.log(bar !== null && typeof bar === "object" && toString.call(bar)!=="[object Array]");// false
或
console.log(bar !== null && typeof bar === "object" && !(bar instanceof Array));// false
或
console.log(bar !== null && typeof bar === "object" && !(Array.isArray(bar)));// false
```
> Array.isArray()：ES5新增加的判断是否为数组的方法
instanceof：运算符用来判断一个构造函数的prototype属性所指向的对象是否存在另外一个要检测对象的原型链上