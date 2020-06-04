# fetch发送2次请求的原因

!> 预检(Preflighted)的跨域请求

**当HTTP请求出现以下两种情况时，浏览器认为是带预检(Preflighted)的跨域请求：**

- 除GET、HEAD和POST(only with application/x-www-form-urlencoded, multipart/form-data, text/plain Content-Type)以外的其他HTTP方法。
- 请求中出现自定义HTTP头部。

> 带预检(Preflighted)的跨域请求需要浏览器在发送真实HTTP请求之前先发送一个OPTIONS的预检请求，检测服务器端是否支持真实请求进行跨域资源访问，真实请求的信息在OPTIONS请求中通过Access-Control-Request-Method Header和Access-Control-Request-Headers Header描述，此外与简单跨域请求一样，浏览器也会添加Origin Header。
> 服务器端接到预检请求后，根据资源权限配置，在响应头中放入Access-Control-Allow-Origin Header、Access-Control-Allow-Methods和Access-Control-Allow-Headers Header，分别表示允许跨域资源请求的域、请求方法和请求头。此外，服务器端还可以加入Access-Control-Max-Age Header，允许浏览器在指定时间内，无需再发送预检请求进行协商，直接用本次协商结果即可。浏览器根据OPTIONS请求返回的结果来决定是否继续发送真实的请求进行跨域资源访问。这个过程对真实请求的调用者来说是透明的。
