# webpack 中，filename 和 chunkFilename 的区别?

### Module

!> filename 是一个很常见的配置，就是对应于 entry 里面的输入文件，经过webpack 打包后输出文件的文件名

### chunkFilename

!> 未被列在 entry 中，却又需要被打包出来的 chunk 文件的名称。一般来说，这个 chunk 文件指的就是要懒加载的代码。

**参考资料：**
[webpack概念术语](https://webpack.docschina.org/glossary)

**题目来源：**
[webpack 中那些最易混淆的 5 个知识点](https://juejin.im/post/5cede821f265da1bbd4b5630)