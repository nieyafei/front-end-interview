# HTML5中的datalist是什么？

> `<datalist> `标签定义选项列表

> 请与 input 元素配合使用该元素，来定义 input 可能的值

> datalist 及其选项不会被显示出来，它仅仅是合法的输入值列表

```html
<input id="myCar" list="cars" />
<datalist id="cars">
  <option value="BMW">
  <option value="Ford">
  <option value="Volvo">
</datalist>
```

**参考资料：**

[HTML 5 <datalist> 标签](http://www.w3school.com.cn/html5/html5_datalist.asp)