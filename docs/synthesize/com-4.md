# webpackPrefetch、webpackPreload 和 webpackChunkName 到底是干什么的？

### webpackPrefetch

!> 浏览器闲置下载文件

### webpackPreload

!> 会在父 chunk 加载时并行下载文件

### webpackChunkName

!> 新 chunk 的名称。从 webpack 2.6.0 开始，[index] and [request] 占位符，分别支持赋予一个递增的数字和实际解析的文件名。


**参考资料：**
[webpack magic comments](https://webpack.docschina.org/api/module-methods/#magic-comments)

**题目来源：**
[webpack 中那些最易混淆的 5 个知识点](https://juejin.im/post/5cede821f265da1bbd4b5630)