# span标签的width和height分别为多少？

```html
<div style=”width:400px;height:200px;”>
  <span style=”float:left;width:auto;height:100%;”>
    <i style=”position:absolute;float:left;width:100px;height:50px;”>hello</i>
  </span>
</div>
```
**问题：span标签的width和height分别为多少？**

- A. width = 0px，height = 0px
- B. width = 400px，height = 200px
- C. width = 100px，height = 50px
- D. width = 0px，height = 200px

?> `答案：` D

**解析：**

> `span`元素因为`float`之后会变成`行内块级元素`(默认宽度是auto)，因此`height:100%`  也就是父级元素的`200px`

> `i`元素因为`absolute`之后会脱离文档流, 因而不占用正常的文档流，`span`下面没有其他元素，`width`就是`0`, 这也就是`塌陷现象`

**参考资料：**

[题目来源](https://www.nowcoder.com/questionTerminal/8c6c959221d84380804a0c5cd96ba888?toCommentId=1243383)