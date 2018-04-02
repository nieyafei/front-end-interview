# Font-end-interview-js

[![Build Status](https://travis-ci.org/nieyafei/front-end-interview-js.svg?branch=master)](https://travis-ci.org/nieyafei/front-end-interview-js)
[![MIT Licence](https://badges.frapsoft.com/os/mit/mit.svg?v=103)](https://opensource.org/licenses/mit-license.php)

前端面试interview的Js题目收集，持续更新，勿浅尝辄止

- [在线访问](http://codehtml.cn/front-end-interview-js/)

### clone或者Fork之后clone到本地

### 安装环境
> npm i docsify-cli -g

### 启动本地查看
> docsify serve docs

### 面试题列表

* <strong>你必须知道的Js面试题</strong>
  * [1、typeof bar潜在陷阱 <i class='iconS'></i><i class='iconS'></i><i class='iconS'></i>](./docs/basic.md)
  * [2、代码块1：下面的代码将输出到控制台，为什么？](./docs/mustKnow/mk-1.md)
  * [3、代码块2：this有关代码块输出结果？<i class='iconS'></i><i class='iconS'></i><i class='iconS'></i>](./docs/mustKnow/mk-2.md)
  * [4、为什么要用立即执行函数表达式（Immediately-Invoked Function Expression）?](./docs/mustKnow/mk-3.md)
  * [5、严格模式下进行 Javascript 开发有什么好处？](./docs/mustKnow/mk-4.md)
  * [6、两个函数运行结果一样吗？为什么？](./docs/mustKnow/mk-5.md)
  * [7、NaN 是什么？typeof 的结果是？如果判断一个变量的值是 NaN？](./docs/mustKnow/mk-6.md)
  * [8、解释一下下面有关浮点数代码的输出?](./docs/mustKnow/mk-7.md)
  * [9、写一个方法 isInterger(x)，可以用来判断一个变量是否是整数](./docs/mustKnow/mk-8.md)
  * [10、在下面的代码中，数字 1-4 会以什么顺序输出？为什么会这样输出？](./docs/mustKnow/mk-9.md)
  * [11、写一个少于 80 字符的函数，判断一个字符串是不是回文字符串](./docs/mustKnow/mk-10.md)
  * [12、写一个按照下面方式调用都能正常工作的 sum 方法](./docs/mustKnow/mk-11.md)
  * [13、根据下面的代码片段回答后面的问题<i class='iconS'></i>](./docs/mustKnow/mk-12.md)
  * [14、假设`变量d`是一个空的对象(object)](./docs/mustKnow/mk-13.md)
  * [15、下面的代码块会输出什么？为什么？](./docs/mustKnow/mk-14.md)
  * [16、下面的代码块会输出什么？为什么？](./docs/mustKnow/mk-15.md)
  * [17、如果数组列表太大，下面的递归代码将导致堆栈溢出。您如何修复并保留递归模式？](./docs/mustKnow/mk-16.md)
  * [18、什么是闭包（closure）？](./docs/mustKnow/mk-17.md)
  * [19、下面代码块会输出什么？](./docs/mustKnow/mk-18.md)
  * [20、请解释下面代码块的输出结果](./docs/mustKnow/mk-19.md)
  * [21、执行以下代码时输出是什么？解释一下为什么？](./docs/mustKnow/mk-20.md)
  * [22、执行以下代码时输出是什么？解释一下为什么？](./docs/mustKnow/mk-21.md)
  * [23、下面代码块输出结果是多少？](./docs/mustKnow/mk-22.md)
  * [24、下面的代码块，会输出什么？为什么？](./docs/mustKnow/mk-23.md)
  * [25、执行以下代码时输出是什么？解释一下为什么？](./docs/mustKnow/mk-24.md)
  * [26、创建一个函数，给定页面上的DOM元素，将访问元素本身和它的所有后代（不只是其直系子女）。对于所访问的每个元素，函数应该将该元素传递给所提供的回调函数。](./docs/mustKnow/mk-25.md)
  * [27、用JavaScript测试你的知识：以下代码的输出是什么？<span class='new'></span>](./docs/mustKnow/mk-26.md)
  * [28、下面的代码块，会输出什么？为什么？<span class='new'></span>](./docs/mustKnow/mk-27.md)
  * [28、下面的代码块，会输出什么？](./docs/mustKnow/mk-28.md)
  * [30、如何克隆一个Object对象？](./docs/mustKnow/mk-29.md)
  * [31、下面的代码块，会输出什么？](./docs/mustKnow/mk-30.md)
  * [32、执行以下代码时输出是什么？解释一下为什么？](./docs/mustKnow/mk-31.md)
  * [33、如何在数组的开头添加元素？你怎么在结尾加上一个？](./docs/mustKnow/mk-32.md)
  * [34、下面有个代码块，根据赋值查看结果](./docs/mustKnow/mk-33.md)
  * [35、typeof undefined == typeof NULL的结果？](./docs/mustKnow/mk-34.md)
  * [36、下面代码会返回什么？](./docs/mustKnow/mk-35.md)
  * [37、下面的代码块，会输出什么？为什么？<span class='new'></span>](./docs/mustKnow/mk-36.md)

* <strong>Js基础</strong>
  * [NaN 是什么？它的类型是什么？你如何可靠地测试一个值是否等于 NaN ？](./docs/js-nan.md)
  * [<span></span>记忆化斐波那契函数（Memoization）](./docs/js-memoi.md)
  * [javascript有哪几种数据类型](./docs/basic/js-1-2.md)
  * [写一个函数，满足curry(fn)(1)(2)(3)](./docs/basic/js-1-3.md)
  * [undefined与null的区别](./docs/basic/js-1-7.md)
  * [如何获取UA？](./docs/basic/js-1-8.md)

* <strong>原型、原型链、继承、作用域</strong>
  * [什么是原型，原型有什么特点?](./docs/basic/pro-1.md)
  * [什么是原型链，原型链有什么特点?](./docs/basic/pro-2.md)
  * [创建“内置”方法 <i class='iconS'></i><i class='iconS'></i>](./docs/basic/js-1-1.md)
  * [字符串增加原型方法spacify](./docs/string-1.md)
  * [使用原生JS实现Number原型链方法](./docs/basic/js-1-4.md)
  * [代码片段，请输出结果？](./docs/basic/js-1-5.md)

* <strong>闭包</strong>
  * [<span></span>代码片段输出什么？<i class='iconS'></i><i class='iconS'></i>](./docs/bb-1.md)

* <strong>this</strong>
  * [对于this对象的理解](./docs/this/this-7.md)
  * [经典关于this面试知识点题目](./docs/this/this-6.md)
  * [1、代码块题](./docs/this/this-2.md)
  * [2、代码块题](./docs/this/this-3.md)
  * [3、代码块题](./docs/this/this-4.md)
  * [4、代码块题](./docs/this/this-5.md)
  
* <strong>Array</strong>
  * [找出数字数组中最大的元素（使用Math.max函数）](./docs/array/array-5.md)
  * [下面代码块输出结果？](./docs/array/array-1.md)
  * [编写一个函数，进行数组去重](./docs/array/array-2.md)
  * [数组的原生方法有哪些？](./docs/array/array-3.md)
  * [如何判断一个变量是否为数组？<i class='iconS'></i><i class='iconS'></i>](./docs/array/array-4.md)

* <strong>Promise</strong>
  * [<span></span>代码块（阿里二面）<span class="new"></span>](./docs/promise-1.md)

* <strong>正则表达式Regexp</strong>
  * [检验一个字符串首尾是否含有数字 <i class='iconS'></i><i class='iconS'></i>](./docs/regexp/regexp-1.md)
  * [对字符串var str = "1000000000" 进行科学计数法](./docs/regexp/regexp-2.md)
  * [判断字符串是否包含数字](./docs/regexp/regexp-4.md)
  * [判断是否符合 USD 格式](./docs/regexp/regexp-5.md)
  * [对连字符串转换为驼峰命名法](./docs/regexp/regexp-6.md)
  * [判断是否以元音字母结尾](./docs/regexp/regexp-7.md)
  * [邮政编码的验证（开头不能为0，共6位）](./docs/regexp/regexp-8.md)
  * [匹配ip地址](./docs/regexp/regexp-9.md)
  * [检测人民币金额，两位小数](./docs/regexp/regexp-10.md)

* <strong>Js Coding</strong>
  * [判断工具代码技巧](./docs/codes.md)

* <strong>JavaScript Puzzlers!(Js谜题)</strong>
  * [当parseInt遇到map](./docs/reallyKnow/rk-1.md)
  * [关于null](.docs/reallyKnow/rk-2.md)
  * [对于愤怒的reduce](.docs/reallyKnow/rk-3.md)
  * [头痛的优先级](.docs/reallyKnow/rk-4.md)
  * [神鬼莫测之变量提升](.docs/reallyKnow/rk-5.md)
  * [死循环陷阱](.docs/reallyKnow/rk-6.md)
  * [过滤器魔法](.docs/reallyKnow/rk-7.md)
  * [警惕IEEE 754标准](.docs/reallyKnow/rk-8.md)
  * [字符串陷阱](.docs/reallyKnow/rk-9.md)
  * [并非都是奇偶](.docs/reallyKnow/rk-10.md)
  * [parseInt小贼](.docs/reallyKnow/rk-11.md)
  * [数组原型是数组](.docs/reallyKnow/rk-12.md)
  * [强制转换](.docs/reallyKnow/rk-13.md)
  * [关于“==”](.docs/reallyKnow/rk-14.md)
  * [加号 VS 减号](.docs/reallyKnow/rk-15.md)
  * [该死的代码加减](.docs/reallyKnow/rk-16.md)
  * [淘气的map](.docs/reallyKnow/rk-17.md)
  * [<span></span>对于arguments](.docs/reallyKnow/rk-18.md)
  * [损失精度的IEEE 754](.docs/reallyKnow/rk-19.md)
  * [反转reverse](.docs/reallyKnow/rk-20.md)
  * [最小的正值](.docs/reallyKnow/rk-21.md)
  * [谨记优先级](.docs/reallyKnow/rk-22.md)
  * [最经典的WTF](.docs/reallyKnow/rk-23.md)
  * [小数点魔法](.docs/reallyKnow/rk-24.md)
  * [自动提升为全局变量](.docs/reallyKnow/rk-25.md)
  * [正则表达式](.docs/reallyKnow/rk-26.md)
  * [数组比大小](.docs/reallyKnow/rk-27.md)
  * [原型把戏](.docs/reallyKnow/rk-28.md)
  * [构造函数的函数](.docs/reallyKnow/rk-29.md)
  * [禁止修改函数名](.docs/reallyKnow/rk-30.md)
  * [替换(replace)陷阱](.docs/reallyKnow/rk-31.md)
  * [Function的名字](.docs/reallyKnow/rk-32.md)
  * [正则test陷阱](.docs/reallyKnow/rk-33.md)
  * [逗号定义数组](.docs/reallyKnow/rk-34.md)
  * [保留字 class](.docs/reallyKnow/rk-35.md)
  * [无效日期](.docs/reallyKnow/rk-36.md)
  * [神鬼莫测的函数长度](.docs/reallyKnow/rk-37.md)
  * [Date的面具](.docs/reallyKnow/rk-38.md)
  * [min与max共舞](.docs/reallyKnow/rk-39.md)
  * [警惕全局匹配](.docs/reallyKnow/rk-40.md)
  * [熟悉到陌生的Date](.docs/reallyKnow/rk-41.md)
  * [匹配隐式转换](.docs/reallyKnow/rk-42.md)
  * [重复声明变量](.docs/reallyKnow/rk-43.md)

* <strong>必看题目</strong>
  * [<span></span>setTimeout面试连击题](./docs/important-1.md)
  * [涉及同步、异步、作用域、闭包四连问](./docs/important/im-2.md)

* <strong>其他</strong>
  * [Emoji自用-MarkDown](./docs/emoji.md)