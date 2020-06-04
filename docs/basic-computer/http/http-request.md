# HTTP的请求方法

?> HTTP1.0定义了三种请求方法： GET, POST 和 HEAD方法

?> HTTP1.1新增了五种请求方法：OPTIONS, PUT, DELETE, TRACE 和 CONNECT 方法

`GET`

> 请求指定的页面信息，并返回实体主体

`POST`

> 向指定资源提交数据进行处理请求（例如提交表单或者上传文件）。数据被包含在请求体中。POST请求可能会导致新的资源的建立和/或已有资源的修改

`HEAD`

> 类似于get请求，只不过返回的响应中没有具体的内容，用于获取报头

`OPTIONS`

> 允许客户端查看服务器的性能

`PUT`

> 从客户端向服务器传送的数据取代指定的文档的内容

`DELETE`

> 请求服务器删除指定的数据

`TRACE`

> 回显服务器收到的请求，主要用于测试或诊断

`CONNECT`

> HTTP/1.1协议中预留给能够将连接改为管道方式的代理服务器

**参考资料：**

[HTTP请求方法](http://www.runoob.com/http/http-methods.html)