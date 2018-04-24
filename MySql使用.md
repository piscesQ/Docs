##MySql的使用##
---关键字--- 命令行

##### 安装mysql、卸载、修改密码
1、见“参考链接-1”，进入mysql命令：`mysql -u root -p`
2、常用命令，见“参考链接-3”，如下：<br/>
```
sudo /usr/local/mysql/support-files/mysql.server start

sudo /usr/local/mysql/support-files/mysql.server stop

sudo /usr/local/mysql/support-files/mysql.server restart
```

**注意：**如果关闭或启动失败，可以使用`kill -9`命令强行杀死进程

4、卸载MySql:`http://www.jianshu.com/p/b02be6026a2a`;
5、mysql进程杀死之后立即重启的原因: 存在守护进程,位置: `/Library/LaunchDaemons`
6、修改mysql的root用户密码:`http://www.jianshu.com/p/ba7cf5fcf4e5`


### 常用操作 - 命令行
0、参考：`http://www.jianshu.com/p/52c1fa25664c` <br/>
1、登录：`mysql -u root -p` "root"是用户名，然后输入密码，出现提示符`sql>>`说明登录成功！ <br/>
2、退出MYSQL命令： `exit` <br/>
3、显示所有的数据库：`show databases;` <br/>
4、选择需要操作的数据库：`use 名称;`， <br/>
5、创建数据库：`create database 名称;`创建数据库 <br/>
6、导入sql文件，首先选中一个操作的数据库，然后执行命令：`source 文件路径`
7、查看当前使用的数据库：`select database();`


### 常见问题
&emsp;&emsp;&emsp;&emsp;1、命令行和Navicat中其中一个客户端出现乱码 <br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**出现原因**：两个客户端编码不一致导致 <br/>
&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**解决方案**：将Navicat中的数据库连接里面的编码设置成”Auto“即可！！！！ <br/>
&emsp;&emsp;&emsp;&emsp;2、mysql中文乱码问题，**参考**：`http://www.jianshu.com/p/e4923a6b1b3b` 、`http://www.jianshu.com/p/52c1fa25664c` <br/>

### 参考链接
1、Mac下安装与配置MySQL（可用）：`http://www.cnblogs.com/xiaozhiblog/p/5664521.html` <br/>
2、mac上终端启动MySQL的方法：`http://www.cnblogs.com/weilaikeji/archive/2013/05/30/3107836.html` <br/>
3、Mac,Linux命令行下启动停止MySQL：`https://coolestguidesontheplanet.com/start-stop-mysql-from-the-command-line-terminal-osx-linux/` <br/>