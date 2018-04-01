# 判断是否以元音字母结尾

> 1、元音字母包括 a，e，i，o，u，以及对应的大写

> 2、包含返回 true，否则返回 false 

```js
function endsWithVowel(str) {
  return /[a,e,i,o,u]$/i.test(str);
}
```

?> 确定元音集合`[a,e,i,o,u]`