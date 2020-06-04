# 如何实现浏览器内多个标签页之间的通信? (阿里)

> WebSocket、SharedWorker；

> 也可以调用localstorge、cookies等本地存储方式；

> localstorge另一个浏览上下文里被添加、修改或删除时，它都会触发一个事件

> 我们通过监听事件，控制它的值来进行页面信息通信；

> 注意quirks：Safari 在无痕模式下设置localstorge值时会抛出 QuotaExceededError 的异常；

### 下面是一个解答[原文](http://blog.csdn.net/lxcao/article/details/52777066)

- #### **使用localStorage**

使用localStorage.setItem(key,value);添加内容

使用storage事件监听添加、修改、删除的动作   

```
window.addEventListener("storage",function(event){  
        $("#name").val(event.key+”=”+event.newValue);  
}); 
```

- #### **使用cookie+setInterval**

`Html`
```
<inputidinputid="name"><input type="button" id="btnOK"value="发送">  
```

`页面1：js`

```
$(function(){  
  $("#btnOK").click(function(){  
    varname=$("#name").val();  
    document.cookie="name="+name;  
  });  
});  
```

`页面2：js`

```
//获取Cookie天的内容  
function getKey(key) {  
    return JSON.parse("{\""+ document.cookie.replace(/;\s+/gim,"\",\"").replace(/=/gim, "\":\"") +"\"}")[key];  
}  
//每隔1秒获取Cookie的内容  
setInterval(function(){  
    console.log(getKey("name"));  
 },1000);  
```