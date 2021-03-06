# vickze-cloud-admin


中后台前后端分离解决方案，后端基于Spring Cloud开发，前端采用ant-design-pro，主要解决微服务架构多系统下的权限控制，目前包括权限控制中心、代码生成


### 环境

* mysql、redis、alibaba nacos
* jdk1.8
* IDE lombok插件

### 启动步骤

* 初始化 vickze-auth/init.sql、vickze-generator/init.sql
* 启动mysql、redis、alibaba nacos
* 各个服务注释的配置导入到alibaba nacos
* 启动AuthApplication、GeneratorApplication、GatewayApplication
* 启动前端工程 [https://github.com/vickze/vickze-auth-ui](https://github.com/vickze/vickze-auth-ui) [https://github.com/vickze/vickze-generator-ui](https://github.com/vickze/vickze-generator-ui) 账号密码 admin/admin

### 单点启动
* 启动前端工程[https://github.com/vickze/vickze-sso-ui](https://github.com/vickze/vickze-sso-ui)
* vickze-auth-ui、vickze-generator-ui根据单点启动命令启动
* 启动SSOApplication并修改配置sso.system为前端地址

### 功能截图

权限控制中心

![](https://raw.githubusercontent.com/vickze/vickze-cloud-admin/master/images/menuResource.png)

![](https://raw.githubusercontent.com/vickze/vickze-cloud-admin/master/images/menuResource_edit.png)

代码生成系统

![](https://raw.githubusercontent.com/vickze/vickze-cloud-admin/master/images/code.png)

![](https://raw.githubusercontent.com/vickze/vickze-cloud-admin/master/images/config.png)



#### 关于领域驱动设计(DDD,Domain-Driven Design)的理解应用

在前后端分离下所有传输的对象都可以理解成DTO

在本项目中只存在DO、DTO，并且DO可以满足的时候，不另建DTO
