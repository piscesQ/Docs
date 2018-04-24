##Mac软件汇总##
---关键字--- 软件

###APP下载网站推荐
&emsp;&emsp;&emsp;&emsp;1、http://xclient.info/ <br/>
&emsp;&emsp;&emsp;&emsp;2、https://www.macpeers.com/ <br/>
&emsp;&emsp;&emsp;&emsp;3、http://www.waitsun.com/ <br/>
&emsp;&emsp;&emsp;&emsp;4、苹果软件园：http://www.maczapp.com/ <br/>
&emsp;&emsp;&emsp;&emsp;5、维奥网：http://www.weiosx.com/ <br/>



###常见问题
&emsp;&emsp;&emsp;&emsp;1、macOS Sierra (10.12)版本后在“System Preferences"的 “Security & Privacy” 中不再有 “Anywhere” 选项。**解决方法：**在Terminal中输入如下命令：
`sudo spctl --master-disable`

&emsp;&emsp;&emsp;&emsp;2、打开新的Finder默认会显示“All My Files”，此时会生成所有文件的列表，耗时很久，造成卡顿。**解决方案：** 打开Finder --> Preferences --> General --> New Finder windows show 改成你需要显示的目录即可，此处我选择的是我的用户目录

&emsp;&emsp;&emsp;&emsp;3、“XXX.app” can’t be opened because it is from an unidentified developer。**解决方案：** （1）临时方案：右键点击App，选择打开；（2）永久方法：在“Security & Privacy”选择“Anywhere”，参考“常见问题-1”

###Android Mac 文件传输工具
#####1、Android File Transfer - Google
######优缺点
&emsp;&emsp;优：不需要在Android设备上安装软件

&emsp;&emsp;优：适应性和兼容性更强

&emsp;&emsp;缺：传输限制小于4G
######如何关闭自动启动
http://blog.iderzheng.com/disable-auto-start-of-android-file-transfer/

#####2、HandShaker - 锤子科技
######优缺点
&emsp;&emsp;优：界面简洁，体验好；

&emsp;&emsp;优：没有传输文件大小的限制；

&emsp;&emsp;缺：需要在Android设备上安装apk；


###Proxychains
######描述
&emsp;&emsp;终端代理软件
######安装和配置
&emsp;&emsp;1、安装，执行命令：`brew install proxychain-ng` ， 我安装的版本是4.12<br/>
&emsp;&emsp;2、修改配置文件，路径：`/usr/local/etc/proxychains.conf`，在 [ProxyList] 下面，加入代理类型，代理地址和端口，例如使用ss，则修改成`socks5  127.0.0.1 1080`<br/>
&emsp;&emsp;3、测试，命令行输入：`proxychains4 curl twitter.com`，连接成功即可。


###Shortcat
######描述
&emsp;&emsp;使用键盘替代鼠标或触摸板操作的软件，减少鼠标或触摸板的操作次数，提高效率。

######注意事项
&emsp;&emsp;1、安装完成后需要开启Accessibility，操作步骤：System Preferences --> Security&Privacy --> Privacy，点击左下角的小锁，输入密码后，勾选Shortcat前面的对号即可，参考链接：`http://mizage.com/help/accessibility.html`

######使用方法
&emsp;&emsp;1、按下快捷键「Command + Shift + Space」后，当前应用(或窗口)底部会出现一个输入框;

&emsp;&emsp;2、在输入框中输入英文符号「.」，可显示**所有**可点击项;

&emsp;&emsp;3、按 Control + 对应字母，即可选中对应选项;

&emsp;&emsp;4、按下回车键，即为鼠标左键「点击」该选项。


###参考链接
&emsp;&emsp;&emsp;&emsp;1、How to Enable Accessibility on Mac OS X：http://mizage.com/help/accessibility.html


&emsp;&emsp;&emsp;&emsp;2、高效 MacBook 工作环境配置：http://xialeizhou.com/2019/06/23/%E9%AB%98%E6%95%88macbook%E5%B7%A5%E4%BD%9C%E7%8E%AF%E5%A2%83%E9%85%8D%E7%BD%AE/#more

&emsp;&emsp;&emsp;&emsp;3、QQ稳定版下载地址：http://im.qq.com/macqq/support.html

&emsp;&emsp;&emsp;&emsp;4、！！9个小窍门让OS X中Finder用起来更顺手：http://digi.tech.qq.com/a/20130309/000051.htm

&emsp;&emsp;&emsp;&emsp;5、Mac OS X Lion Spotlight 优化指南：http://r12f.com/posts/Mac-OS-X-Lion-Spotlight-%E4%BC%98%E5%8C%96%E6%8C%87%E5%8D%97/



###我的软件列表
#####系统增强

Bartender 2.app     Mac顶部导航条图标管理工具<br/>
Caffeine.app			系统休眠控制工具<br/>
CleanMyMac 3.app    清理软件<br/>
CopyClip 2.app      保存复制记录，并快速复制<br/>
Go2Shell.app        在当前目录下打开命令行<br/>
PopClip.app		   增强的复制工具<br/>
ShadowsocksX.app   sock代理<br/>
Proxychains   终端代理软件<br/>
Lantern.app		  免费开源代理<br/>
SizeUp.app        多屏管理软件<br/>
StatsCenter.app   电脑状态监控软件（cpu、memory等）<br/>
iTerm.app    Mac终端软件，功能强大<br/>
Shortcat.app   减少使用触摸板频率的软件、键盘功能增强<br/>
XtraFinder.app  Finder扩展插件<br/>
Path Finder.app 增强版Finder<br/>
Manico.app   应用快速切换工具，功能类似Windows上的“Win + Tab”<br/>
CheatSheet.app  显示当前软件的所有快捷键（按住command）<br/>
Stickies.app  便签<br/>
Paragon NTFS for Mac 14.app  兼容NTFS格式U盘，使U盘可读写（卸载方法：在“System Preferences”最下面的ParagonNTFS中的“setting”标签下卸载即可）<br/>


#####效率软件

Alfred.app     神器 - 效率工具<br/>
Evernote.app   印象笔记<br/>
IntCalc.app    科学计算器<br/>
Sip.app        取色软件<br/>
Wunderlist.app  清单<br/>
Automator.app   系统自带的工作流软件<br/>
TickTick.app  滴答清单，增强版备忘录，提醒功能强大<br/>

#####日常软件

Airmail 3.app   邮件客户端；优：界面体验好；<br/>
Foxmail.app     邮件客户端；缺：不支持Gmail<br/>
Fantastical 2.app	最好用的日历软件<br/>
Folx GO.app  下载工具；（可以被aria2取代）<br/>
BitTorrent Sync.app  BT下载（可以被aria2取代）<br/>
HideAway.app  格式转换工具<br/>
有道词典.app  <br/>
FileZilla.app 一款FTP软件，类似Win上的FlashFXP <br/>

#####压缩软件

BetterZip.app 解压软件；缺：偶尔出现乱码情况<br/>
The Unarchiver.app  解压软件；缺：只能直接解压，不能查看压缩包内部文件；使用场景：BetterZip出现乱码时使用<br/>


#####文档

MacDown.app   markdown编辑器；优：启动速度快、方便；缺：预览效果欠缺<br/>
**Quiver.app**   文档编辑器；优：支持多种编辑格式，可以导出多种格式；<br/>
Haroopad.app   markdown编辑器；优：预览效果好；缺：启动速度慢；（不推荐使用）<br/>
Microsoft Offical 系列<br/>
PDF Expert.app   pdf查看工具，有添加注释、标记功能<br/>
XMind.app  思维导图工具<br/>

#####开发软件

Android Studio.app<br/>
IntelliJ IDEA.app<br/>
WebStorm.app<br/>

#####开发工具

Charles.app   抓包工具<br/>
Dash.app     各种语言文档<br/>
Genymotion.app   Android虚拟机<br/>
GitHub Desktop.app<br/>
JD-GUI.app   jar包查看工具<br/>
Paw.app   模拟发送网络请求，类似postman<br/>
noodle.app   Telnet、SSH、rlogin、纯TCP以及串行接口连接软件，类似Windows上的putty<br/>
Wireshark.app   抓包工具，比charles更底层<br/>
VMware Fusion.app  虚拟机<br/>

#####工程、反编译、安全
StakePoint Projects.app  项目分析优化软件 <br/>
Hex Fiend.app  十六进制编辑器 <br/>
Hopper Disassembler v3.app  反编译软件<br/>
Tyrhex.app  反编译 - 文件数据取证工具<br/>

#####版本控制、团队协作

Cornerstone.app   最好用的svn客户端<br/>
SimpleGitServer.app  Git服务器<br/>
SourceTree.app  git客户端（推荐使用命令行）<br/>
LeanChat.app 团队沟通协作工具 <br/>
Quip.app  团队协作的写作工具 <br/>

#####文本工具

Atom.app 文本编辑器<br/>
Sublime Text.app 文本编辑器<br/>

#####影音图片

TinyPNG4Mac.app   图片压缩客户端<br/>
Cook App Icon.app  快速转换应用图标工具<br/>
Snip.app   截图工具<br/>
Xee³.app   图片浏览工具<br/>
Jietu.app   截图工具<br/>
Instant Convert.app 图片格式转换工具 <br/>
Instant Resize.app  图片大小调整工具<br/>
LICEcap.app 简易的GIF图片制作工具,无须图片,直接可以将屏幕录制生成GIF图 <br/>
ProPaint.app  图片查看编辑工具，类似windows中的画图，支持psd <br/>

Movist.app 视频播放器<br/>
QuickTime Player.app  视频播放器<<br/>
Final Cut Pro_10.3_xclient.info 专业视频处理 <br/>

#####浏览器

TorBrowser.app  暗网浏览器<br/>
Google Chrome Canary.app<br/>

#####其他软件

Font Book.app  字体库<br/>