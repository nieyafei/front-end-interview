# 代码块题

### 写出打印结果

```js
function Person(name, age, sex) {
  var a = 0;// 私有化变量
  this.name = name;
  this.age = age;
  this.sex = sex;
  function sss() {
    a ++;
    console.log(a);
  }
  this.say = sss;
}
var oPersopn = new Person();
oPersopn.say();// 打印结果？
oPersopn.say();// 打印结果？
var oPersopn1 = new Person();
oPersopn1.say();// 打印结果？

```

`结果：`

> 1    2    1