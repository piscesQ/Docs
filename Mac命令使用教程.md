##Mac命令使用教程
---关键字--- netstat lsof ps

#####Mac OS/Linux命令查询网络端口占用情况
&emsp;&emsp;&emsp;&emsp;1、`netstat -an | grep 端口号`<br/>
&emsp;&emsp;&emsp;&emsp;2、`lsof -i:端口号`，-i参数表示网络链接，:80指明端口号，该命令会同时列出PID，方便杀死进程，命令：`kill -9 进程的PID`
&emsp;&emsp;&emsp;&emsp;参考链接：`http://www.cnblogs.com/kaiye/archive/2013/05/25/3099393.html` <br/>
3、检查mysql是否有实例运行：`ps -ef | grep mysql
` <br/>






###参考链接

&emsp;&emsp;&emsp;&emsp;1、Mac OS X Terminal 101：终端使用初级教程：`https://www.renfei.org/blog/mac-os-x-terminal-101.html` <br/>
&emsp;&emsp;&emsp;&emsp;2、**zch教程文档**：`https://wiki.archlinux.org/index.php/Zsh_(%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87)` <br/>
&emsp;&emsp;&emsp;&emsp;3、Mac常用命令汇总：`http://www.jianshu.com/p/3291de46f3ff`  <br/>
&emsp;&emsp;&emsp;&emsp;4、**每天一个linux命令目录**：`http://www.cnblogs.com/peida/archive/ 2012/12/05/2803591.html` <br/>
