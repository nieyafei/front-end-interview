# webpack 中，module，chunk 和 bundle 的区别是什么？

### Module

!> 提供比完整程序接触面(surface area)更小的离散功能块。精心编写的模块提供了可靠的抽象和封装界限，使得应用程序中每个模块都具有条理清楚的设计和明确的目的。

模块解析(Module Resolution): 一个模块可以作为另一个模块的依赖模块，resolver 是一个库( library )用于帮助找到模块的绝对路径... 模块将在 resolve.modules 中指定的所有目录内搜索。

### Chunk

!> Chunk是 webpack 特定的术语被用在内部来管理 building 过程。bundle 由 chunk 组成，其中有几种类型（例如，入口 chunk(entry chunk) 和子 chunk(child chunk)）。通常 chunk 会直接对应所输出的 bundle，但是有一些配置并不会产生一对一的关系。

### Bundle

!> 由多个不同的模块生成，bundles 包含了早已经过加载和编译的最终源文件版本。

Bundle 分离(Bundle Splitting): 这个流程提供一个优化 build 的方法，允许 webpack 为应用程序生成多个 bundle。最终效果是，当其他某些 bundle 的改动时，彼此独立的另一些 bundle 都可以不受到影响，减少需要重新发布的代码量，因此由客户端重新下载并利用浏览器缓存。

**参考资料：**
[webpack概念术语](https://webpack.docschina.org/glossary)

**题目来源：**
[webpack 中那些最易混淆的 5 个知识点](https://juejin.im/post/5cede821f265da1bbd4b5630)