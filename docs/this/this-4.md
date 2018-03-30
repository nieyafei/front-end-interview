# 代码块题

### 写出打印结果

```js
var fullName = "alibaba";
var obj = {
  fullName:"baidu",
  prop:{
    fullName:"tengxun",
    getFullName: function(){
      return this.fullName;
    }
  }
}
console.log(obj.prop.getFullName());// tengxun
var test = obj.prop.getFullName;
console.log(test());

```

`结果：`

> tengxun alibaba