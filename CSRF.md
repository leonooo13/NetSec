又称跨站请求伪造  
## 原理
未校验请求来源导致攻击者利用用户的信息进行敏感的业务操作  
**比如**：受害者登录网站，发起登录请求，将cookie存储在浏览器中，hacker发送恶意链接，加载恶意脚本，获取cookie，伪造请求。
本站请求伪造：OSRF
可以分为：  
1. CSRF read  json劫持
2. CSRF write  修改数据  
### 攻击手法    
write
dvwa中的源代码如下  
![[Pasted image 20230407213148.png]]
```
http://dvwa.exp-9.com/vulnerabilities/csrf/?password_new=password&password_conf=password&Change=Change#
```
GET方式可以直接嵌入url里  
POST方式中需要自己创建表单
read  
### 测试思路
参数的用途  
### 防御方式
利用post 加token or 验证码
