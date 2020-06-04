# CSS 引入的方式有哪些? link 和@import 的区别是?

**四种：`内联(元素上的style属性)`、`内嵌(style标签)`、`外链(link)`、`导入(@import)`**

### link和@import的区别：

?> **link是XHTML标签，除了加载CSS外，还可以定义RSS等其他事务；@import属于CSS范畴，只能加载CSS。**

?> **link引用CSS时，在页面载入时同时加载；@import需要页面网页完全载入以后加载。**

?> **link是XHTML标签，无兼容问题；@import是在CSS2.1提出的，低版本的浏览器不支持。**

?> **link支持使用Javascript控制DOM去改变样式；而@import不支持。**



