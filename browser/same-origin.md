# 同源限制及跨域

## 1. 同源概念

为了保证用户信息的安全，防止恶意的网站窃取数据产生了同源限制，同源是指三个相同，**协议相同+域名相同+端口相同**，尤其注意`http://www.example.com`和`http://example.com`为不同域名，还有域名和域名对应相同ip也是不同域的。

## 2. 同源限制范围

（1） 无法读取非同源网页的 Cookie、LocalStorage 和 IndexedDB。

（2） 无法接触非同源网页的 DOM。

（3） 无法向非同源地址发送 AJAX 请求（可以发送，但浏览器会拒绝接受响应）

## 3. 跨域方法

>参考资料：[前端常见跨域解决方案（全）](https://segmentfault.com/a/1190000011145364)   [解锁跨域的九种姿势](https://github.com/LiChangyi/crossDomain)   [同源限制及解决](https://wangdoc.com/javascript/bom/same-origin.html)

（1）通过jsonp跨域——只能实现get一种请求

（2）跨域资源共享（CORS）

（3）postMessage跨域——网页之间通信

（4）nginx代理跨域

（5）nodejs中间件代理跨域

（6）WebSocket协议跨域

（7）document.domain + iframe跨域——主域相同，子域不同场景

（8）location.hash + iframe

（9）window.name + iframe跨域

✍️ 要注意 CORS 的两种请求：简单请求和非简单请求（预检请求），参考👉 [全面讲解 CORS](https://juejin.im/post/6856556746706518024#heading-4)

{% hint style="info" %} 前端学习项目之[前端跨域](https://github.com/MrEnvision/Front-end_learning_project/tree/master/cross-domain_solutions) {% endhint %}

