# cookie、sessionSttorage、localStory区别

> `cookie`、`sessionSttorage`、`localStory`都是在客户端以键值对存储的存储机制，并且只能将值存储为字符串

| | cookie | localStorage | sessionStorage |
|:--------:|:--------:|:--------:|:--------:|
|由谁初始化|客户端或服务器，服务器可以使用Set-Cookie请求头。|客户端|客户端|
|过期时间|手动设置	|永不过期|当前页面关闭时|
|在当前浏览器会话（browser sessions）中是否保持不变|取决于是否设置了过期时间|是|否|
|是否与域名（domain）相关联|是|否|否|
|是否随着每个 HTTP 请求发送给服务器|是，Cookies 会通过Cookie请求头，自动发送给服务器|否|否|
|容量（每个域名）|4kb|5MB|5MB|
|访问权限|任意窗口|任意窗口|当前页面窗口|

**题目来源**

[来源链接](https://github.com/yangshun/front-end-interview-handbook/blob/master/Translations/Chinese/README.md)

**参考**

- [https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
- [http://tutorial.techaltum.com/local-and-session-storage.html](http://tutorial.techaltum.com/local-and-session-storage.html)