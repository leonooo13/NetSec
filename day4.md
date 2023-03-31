# `SQL`注入
原理：未对外面的SQL语句进行过滤  
```php
$id=$_REQUEST['id']//输入框中显示的id
$sql="select * from users where id=$id limit 0,1"
```
常见的`URL`地址  
	`www.url.com/index.php`可以能回SQL注入  
	`www.url.com/?id=1`可以能回SQL注入  
	`www.url.com/?id=1&x=2`可以能回SQL注入  
	`www.url.com/index.php`可以能回SQL注入 可能是POST注入  
参数`x`有一下注入测试
	``www.url.com/index.php?y=1&x=2 and 1=1``
注入点后面加`SQL`语句  
	SQLMAP默认后面增加查询语句  
数据库查询
	低版本：暴力差
	高版本：`information_schema`表进行查找  
变量：需要外部传递，可以控制  
攻击方法
1. 回显注入
	回显注入
防御方法：de  
dee

