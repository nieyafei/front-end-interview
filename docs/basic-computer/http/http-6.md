# 描述RARP(Reverse Address Resolution Protocol)协议

?> `RARP`是逆地址解析协议(反向地址转换协议)，作用是完成硬件地址到IP地址的映射，主要用于无盘工作站，因为给无盘工作站配置的IP地址不能保存。

?> 工作流程：在网络中配置一台`RARP`服务器，里面保存着`IP地址`和`MAC地址`的映射关系，当无盘工作站启动后，就封装一个RARP数据包，里面有其MAC地址，然后广播到网络上去，当服务器收到请求包后，就查找对应的MAC地址的IP地址装入响应报文中发回给请求者。因为需要广播请求报文，因此RARP只能用于具有广播能力的网络。

更多详细资料[反向地址转换协议](https://baike.baidu.com/item/%E5%8F%8D%E5%90%91%E5%9C%B0%E5%9D%80%E8%BD%AC%E6%8D%A2%E5%8D%8F%E8%AE%AE/2991811?fr=aladdin&fromid=610685&fromtitle=RARP)

**参考资料：**

[题目来源](https://www.nowcoder.com/ta/review-network/review?tpId=33&tqId=21193&query=&asc=true&order=&page=5)