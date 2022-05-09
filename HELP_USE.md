## 开发/使用👩‍❤️‍👨

1. 编译vue并替换到webapp（注意保留webapp/WEB-INF文件夹）

2. 创建数据库，[数据库表结构](/wall.sql)

3. 修改 [back/src/main/resources/db-template.properties](back/src/main/resources/db-template.properties) 设置数据库

	```properties
	# JDBC
	driver=com.mysql.cj.jdbc.Driver
	# 数据库连接
	url=jdbc:mysql://xxx.xxx.xxx.xxx:3306/xxxx?userSSL=false&useUnicode=true&characterEncoding=UTF-8
	# 数据库账号
	user=xxx
	# 数据库密码
	password=xxx
	```

4. 修改 [back/src/main/resources/email-template.properties](back/src/main/resources/email-template.properties) 设置邮箱SMTP

	```properties
	# 发送邮箱
	emailAccount=xxx
	# 邮箱密码
	emailPassword=xxxx
	# STMP地址
	emailSMTPHost=xxxx
	# STMP端口
	port=25
	# 是否使用SSL
	ssl=false
	# 发送者名称
	sendName=admin
	```



### 接口文档🥰

[接口文档](/HELP_API.md)

[在线文档（Swagger）](https://wall.conststar.cn/swagger-ui/index.html#/)

[开发帮助](/HELP_DEV.md)



### 流程

#### 登录账号

![登录流程](/help/diagraming_登录账号.png)



#### 通过邮箱注册账号

![通过邮箱注册账号流程](/help/diagraming_通过邮箱注册账号.png)



#### 微信登录账号

**临时登录凭证code**获取方法请查阅**微信开发文档**：[wx.login(Object object)](https://developers.weixin.qq.com/miniprogram/dev/api/open-api/login/wx.login.html)

![微信登录流程](/help/diagraming_微信登录.png)



#### 获取帖子列表

同**评论列表**、**搜索帖子列表**等

![获取帖子列表流程](/help/diagraming_获取帖子列表.png)