1. sql is 一个标准  各种sql数据库 遵循sql标准 但未必100%遵循

例如 mysql 就没有全连接 full join  sqlserver中没有 top N

2. 选择mysql原因
	
	6之前是免费的
	
	linux apache mysql php  组成 LAMP架构
	
3. 关注postgresql数据库
	
	开源数据库
	
	sql标准严格
	
4. 客户端与服务端
	
	mysql	客户端
	
	mysqld  服务器端  d daemon 守护服务 后台程序

5. 命令行显示数据乱码
	
	那是因为命令行程序使用字符集与数据库的字符集不一致造成的
	
	例如 windows系统命令行程序字符集默认 GBK字符集 而数据库默认是 utf8字符集
	
	解决办法: set names gbk; 这行代码是告诉mysql服务器请你的utf8字符数据转为GBK字符集返给命令行程序

6. sql语句遇见 ; 认为结束 

7. Error 1064 一定sql语句错误

8. 使用tee记录mysql client 所有的操作
	
	mysql> tee client_mysql.log 
	
9. ERROR 1306 因为客户端没有声明字符集  解决办法 set name 客户端字符集;  告诉服务端 客户端传输过来数据字符集 便于解析