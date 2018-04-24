##SS配置、加速、免流##
---关键字--- ss vps net_speeder

###常用的VPS
&emsp;&emsp;&emsp;&emsp;1、HostUS（HK服务器，虽然不直连，ping大约150ms）

###常用软件
&emsp;&emsp;&emsp;&emsp;1、bestTrace：用来追踪路由，功能类似tracert，支持多平台（Windows、MacOS）

###加速方案
&emsp;&emsp;&emsp;&emsp;net_speeder：简单粗暴，参考`https://www.zrj96.com/post-272.html`

&emsp;&emsp;&emsp;&emsp;查看net-speeder是否运行：`ps aux|grep net_speeder|grep -v grep`。

&emsp;&emsp;&emsp;&emsp;停止net-speeder：`killall net_speeder`。

###参考链接
&emsp;&emsp;&emsp;&emsp;1、Shadowsocks-go一键安装脚本：https://teddysun.com/392.html

&emsp;&emsp;&emsp;&emsp;2、CentOS_6.x的免流服务器搭建-openVPN：http://willis.blog.51cto.com/11907152/1845430

&emsp;&emsp;&emsp;&emsp;3、CentOS 服务器一键安装：http://www.sbwml.cn/vpn/

&emsp;&emsp;&emsp;&emsp;4、科学上网之ss安装及优化加速：http://wuchong.me/blog/2015/02/02/shadowsocks-install-and-optimize/

&emsp;&emsp;&emsp;&emsp;5、**kcptun 完整教程**：https://blog.kuoruan.com/102.html

&emsp;&emsp;&emsp;&emsp;6、**kcptun 教程 - 简书**：http://www.jianshu.com/p/172c38ba6cee

&emsp;&emsp;&emsp;&emsp;7、kcptun - 实现ss加速：https://blog.whsir.com/post-298.html

&emsp;&emsp;&emsp;&emsp;8、FinalSpeed - 实现ss加速：https://mritd.me/2016/01/18/ShadowSocks-FinalSpeed-%E5%8A%A0%E9%80%9F%E6%95%99%E7%A8%8B/

&emsp;&emsp;&emsp;&emsp;9、VPS/服务器优化网络、加速方法总结与参考：https://www.zrj96.com/post-272.html