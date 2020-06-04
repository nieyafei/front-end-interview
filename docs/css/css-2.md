# CSS中居中的几种方式

  > `- 块级居中(block)：`
  margin: 0 auto

>  `- 行级居中（inline,inline-block）`父元素css：text-align: center

> `- 定位水平垂直居中`：left：50%;top:50%;margin-left:负自身宽度的一半;margin-top:负自身高度的一半;

> `- 定位水平垂直居中`：top:0;bottom:0;left:0;right:0;margin:auto;

> `- css3+定位水平垂直居中：left：50%;top:50%;transfrom:(-50%,-50%);`

> `- 水平垂直居中`：diplay：table-cell;vertical-align: middle;

> `- 水平垂直居中`：flexBox居中 display: flex;justify-content: center;align-items:center;

> `- 水平垂直居中`：vertical-align:middle;

**参考资料：**

[盘点8种CSS实现垂直居中水平居中的绝对定位居中技术](http://blog.csdn.net/freshlover/article/details/11579669)