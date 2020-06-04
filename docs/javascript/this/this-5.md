# 5、代码块题

```js

var name = "This window";
var object = {
  name: "My object",
  getFn: function(){
    return function(){
      return this.name;
    }
  },
  getName:function(){
      var that = this;
      return function(){
        console.log(that.name);
      }
  }
}
console.log(object.getFn()());
console.log(object.getName()());
```

**结果：**

```
This window
My object
```


