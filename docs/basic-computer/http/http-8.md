# http的状态码中，499是什么？如何出现499，如何排查跟解决?

> 499错误是什么？

```
ngx_string(ngx_http_error_495_page), /* 495, https certificate error */
ngx_string(ngx_http_error_496_page), /* 496, https no certificate */
ngx_string(ngx_http_error_497_page), /* 497, http to https */
ngx_string(ngx_http_error_404_page), /* 498, canceled */
ngx_null_string,                    /* 499, client has closed connection */
```

- 499对应的是 “client has closed connection”，客户端请求等待链接已经关闭，可能是因为服务器端处理的时间过长，客户端等得“不耐烦”了

- 还有一种是两次提交post过快就会出现499

**解决办法：**

```
- 前端将timeout最大等待时间设置大一些
- nginx上配置proxy_ignore_client_abort on;
```

**题目来源：**

[Github: http的状态码中，499是什么？如何出现499，如何排查跟解决](https://github.com/airuikun/Weekly-FE-Interview/issues/1)