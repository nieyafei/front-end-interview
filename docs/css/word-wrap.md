# word-wrap & text-overflow的区别？
### word-wrap

?> `word-wrap` 属性允许长单词或 URL 地址换行到下一行

?> 语法：`word-wrap: normal|break-word`;

```css
.oneline {
  white-space: nowrap; //强制文本在一行内输出
  overflow: hidden; //隐藏溢出部分
  text-overflow: ellipsis; //对溢出部分加上...
}
```

### text-overflow

?> `text-overflow` 属性规定当文本溢出包含元素时发生的事情

?> 语法：`text-overflow: clip|ellipsis|string`;

#### 多行隐藏（针对webkit内核）

```js
.multiline {
  display: -webkit-box !important;
  overflow: hidden;
  
  text-overflow: ellipsis;
  word-break: break-all;
  
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 2;
}
```

**参考资料：**

·[题目来源](https://segmentfault.com/a/1190000006890725)