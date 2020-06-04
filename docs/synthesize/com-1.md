# 介绍下 npm 模块安装机制，为什么输入 npm install 就可以自动安装对应的模块？

!> npm install

### npm 模块安装机制：

- 发出npm install命令
- 查询node_modules目录之中是否已经存在指定模块

> 若存在，不再重新安装

> 若不存在
- npm 向 registry 查询模块压缩包的网址
- 下载压缩包，存放在根目录下的.npm目录里
- 解压压缩包到当前项目的node_modules目录

### 实现原理

- 执行工程自身 preinstall

- 确定首层依赖模块

- 获取模块

- 模块扁平化（dedupe）

- 安装模块

- 执行工程自身生命周期

**参考资料：**

[npm 模块安装机制简介](http://www.ruanyifeng.com/blog/2016/01/npm-install.html)

[详解npm的模块安装机制](https://www.bbsmax.com/A/qVdemmnEdP/)

[知乎：npm install的实现原理？](https://www.zhihu.com/question/66629910)

**题目来源：**

[介绍下 npm 模块安装机制，为什么输入 npm install 就可以自动安装对应的模块？](https://github.com/Advanced-Frontend/Daily-Interview-Question/issues/22)
