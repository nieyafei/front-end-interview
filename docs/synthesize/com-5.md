# webpack 中，hash、chunkhash、contenthash 有什么不同？

### hash

!> 计算与整个项目的构建相关，构建生成的文件hash值都是一样的，所以hash计算是跟整个项目的构建相关，同一次构建过程中生成的hash都是一样的，只要项目里有文件更改，整个项目构建的hash值都会更改。

### chunkhash

!> 根据不同的入口文件(Entry)进行依赖文件解析、构建对应的chunk，生成对应的哈希值。

### contenthash

!> 计算与文件内容本身相关，由文件内容产生的hash值，内容不同产生的contenthash值也不一样

**参考资料：**
[webpack](https://webpack.docschina.org/concepts/)

**题目来源：**
[webpack 中那些最易混淆的 5 个知识点](https://juejin.im/post/5cede821f265da1bbd4b5630)