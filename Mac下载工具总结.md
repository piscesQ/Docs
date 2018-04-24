##Mac下载工具总结##
---关键字--- aria2 控制程序的显示和隐藏

###aria2
#####安装步骤
&emsp;&emsp;&emsp;1、下载并安装`homebrew`，下载地址：`aria2c项目地址：http://aria2.sourceforge.net`
`aria2c稳定版：http://sourceforge.net/projects/aria2/files/stable`，下载aria2-osx-darwin.dmg 文件，并安装即可

&emsp;&emsp;&emsp;2、该程序属于为认证的开发程序，打开dmg文件后需要按住Control然后点击pkg文件，然后选择“Open”，未认证程序的安装方式，参见`http://www.iclarified.com/28180/how-to-open-applications-from-unidentified-developers-in-mac-os-x-mountain-lion`

&emsp;&emsp;&emsp;3、创建aria2.sh文件，内容如下

<span style="color:red">添加文件内容</span>


&emsp;&emsp;&emsp;4、执行`./aria2.sh start`运行aria2

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;**常用命令：**

`./aria2.sh start:启动aria2进程`
`./aria2.sh stop:停止aria2进程`
`./aria2.sh restart:重启aria2进程`
`./aria2.sh status:检查aria2是否运行`

&emsp;&emsp;&emsp;5、使用命令下载管理页面：`git clone https://github.com/ziahamza/webui-aria2`，下载后打开index.html文件即可

&emsp;&emsp;&emsp;**备注：**命令行安装homebrew，执行命令：`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`， **参考链接：**`http://www.tuicool.com/articles/MfUVV3`

###控制程序的显示和隐藏
`defaults write com.apple.finder AppleShowAllFiles -bool true`       此命令显示隐藏文件

`defaults write com.apple.finder AppleShowAllFiles -bool false`      此命令关闭显示隐藏文件

命令运行之后需要重新加载Finder：快捷键option+command+esc，选中Finder，重新启动即可，或者执行命令`killall Finder`即可

#####参考链接
&emsp;&emsp;&emsp;&emsp;1、如何使用aria2及webui-aria2下载百度云资源：http://moflying.com/2016/06/05/%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8aria2%E5%8F%8Awebui-aria2%E4%B8%8B%E8%BD%BD%E7%99%BE%E5%BA%A6%E4%BA%91%E8%B5%84%E6%BA%90/

&emsp;&emsp;&emsp;&emsp;2、macbook吧：http://tieba.baidu.com/p/4043486441

&emsp;&emsp;&emsp;&emsp;3、github - aria2 - gui：https://github.com/yangshun1029/aria2gui

&emsp;&emsp;&emsp;&emsp;4、Mac 上使用百度网盘很烦躁？花点时间配置 aria2 吧：http://www.chinastor.org/WangPan/7498.html