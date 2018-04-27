**项目说明** 
- 采用SpringBoot、MyBatis、dubbo框架，RESTFUL接口，自定义的功能级权限系统，极低门槛，拿来即用。设计之初，设计之初就为了前后端分离和分布式，方便扩展高效。
- 提供了代码生成器，只需编写30%左右代码，其余的代码交给系统自动生成，可快速完成开发任务
- 配套前端代码地址：https://github.com/chenzhenjian/yum-vue.git
<br>

**具有如下特点** 
- 前后端分离，页面交互使用Vue2.x，极大的提高了开发效率
- restful风格，一套接口供多种客户端调用，极大降低开发成本。
- dubbo作为中间件实现微服务
- 灵活的权限控制，可控制到页面或按钮，满足绝大部分的权限需求
- 完善的部门管理及数据权限，通过注解实现数据权限的控制
- 完善的XSS防范及脚本过滤，彻底杜绝XSS攻击
- 支持分布式部署，session存储在redis中
- 友好的代码结构及注释，便于阅读及二次开发
- 引入quartz定时任务，可动态完成任务的添加、修改、删除、暂停、恢复及日志查看等功能
- 引入swagger文档支持，方便编写API接口文档

<br>

**数据权限设计思想** 
- 管理员管理、角色管理

<br> 

**项目结构** 
```
yum-restful
├─common     公共模块
│ 
├─service-admin      管理后台
│    ├─db  数据库SQL脚本
│    │ 
│    ├─modules  模块
│    │    ├─job 定时任务
│    │    ├─oss 文件存储
│    │    └─sys 系统管理(核心)
│    │ 
│    └─resources 
│        ├─mapper   MyBatis文件
│        ├─statics  静态资源
│        ├─template 系统页面
│        │    ├─modules      模块页面
│        │    ├─index.html   AdminLTE主题风格（默认主题）
│        │    └─index1.html  Layui主题风格
│        └─application.yml   全局配置文件
│       
│ 
├─api-admin        API服务
│ 
├─generator  代码生成器
│        └─resources 
│           ├─mapper   MyBatis文件
│           ├─template 代码生成器模板（可增加或修改相应模板）
│           ├─application.yml    全局配置文件
│           └─generator.properties   代码生成器，配置文件
│
```

<br>

 **技术选型：** 
- 核心框架：Spring Boot 1.5
- 中间件：dubbo
- 服务注册中心zookeeper 3.4
- 持久层框架：MyBatis 3.4
- 数据库连接池：Druid 1.1
- 日志管理：SLF4J 1.7、Log4j
- 页面交互：Vue2.x

<br>

 **软件需求** 
- JDK1.8
- MySQL5.5+
- Maven3.0+

<br>

 **本地部署**
- 通过git下载源码
- 创建数据库keep，数据库编码为UTF-8
- 执行db/mysql.sql文件，初始化数据【按需导入表结构及数据】
- 修改application-dev.yml文件，更新MySQL账号和密码
<br>

- 本地开启redis，开启zookeeper
- Eclipse、IDEA运行ServiceAdminApplication.java，则可启动服务提供者
- Eclipse、IDEA运行ApiAdminApplication.java,则可启动服务消费者，同时开启对外接口http://localhost:8080
- 通过git下载前端源码：https://github.com/chenzhenjian/yum-vue.git
- 使用vscode、webstorm打开项目，在terminal运行npm install，npm run dev
- 浏览器访问 http://localhost:8081
- 账号密码：admin/admin

<br>


 **项目演示**
- 演示地址：暂无
- 账号密码：admin/admin

<br>

**如何交流、反馈、参与贡献？** 
https://github.com/chenzhenjian/yum-restful.git
- 官方QQ群：
<br>

**接口文档效果图：** 
![输入图片说明](http://cdn.renren.io/img/c8dae596146248d8b4d0639738c2932b "在这里输入图片标题")

<br>

