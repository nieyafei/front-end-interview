# 设计一个策略和方法，实现在https的前端项目里进行http请求

**有人提到反向代理，也有人说混合内容**

### 混合内容

!> 使用HTTP的内容包含在一个HTTPS页面内，但它不能改变网页的其他部分。例如，攻击者可以用一个不适当的图像或消息替换网页中一个使用HTTP的图像。攻击者也可以通过提供给用户的图像推断出用户的活动状况；某些图像往往只会在一个网站的一个特定页面上。如果攻击者观察到用户以HTTP请求这些图像，他就可以确定用户正在访问哪些网页。

更详细的答案可以去题目来源看，或者自查资料

**参考资料：**

[混合内容 - 安全 | MDN](https://developer.mozilla.org/zh-CN/docs/Security/MixedContent)

**题目来源：**

[设计一个策略和方法，实现在https的前端项目里进行http请求](https://github.com/airuikun/Weekly-FE-Interview/issues/28)