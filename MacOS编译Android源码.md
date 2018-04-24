## MacOS编译Android源码##
---关键字--- Android源码

### 官方网站
&emsp;&emsp;http://source.android.com/source/initializing.html

&emsp;&emsp;源码准备编译：https://source.android.com/setup/building

&emsp;&emsp;代号、标记和细分版本号：https://source.android.com/source/build-numbers

&emsp;&emsp;驱动：https://developers.google.com/android/drivers

### 环境
&emsp;&emsp;Mac系统：10.11.6
&emsp;&emsp;分支：android-7.1.2_r28 版本号：N2G48C
&emsp;&emsp;设备：Nexus 6P

### 编译步骤
&emsp;&emsp;1、创建一个大小写敏感的分区（格式化为OS X扩展），打开系统自带的“磁盘工具” --> 按住“Ctrl + N” --> 大小为100G，格式为“大小写敏感、日志式 --> 点击“保存” --> 到目录~/Documents
下找到对应的dmg文件，双击即可挂载；动态调整dmg大小命令`hdiutil resize -size <new-size-you-want>g ~/android.dmg`<br/>

&emsp;&emsp;2、在系统自带的“磁盘工具”中点击顶部“Erase”按钮，擦除一次刚刚创建的逻辑分区，格式选择“大小写敏感、日志式” --> 点击顶部的“Info”按钮查看其中的“Is case-sensitive”的值如果是“Yes”则配置正确<br/>

&emsp;&emsp;3、安装软件MacPorts，并将`/opt/local/bin`加入PATH，然后执行`sudo port -d sync`，最后执行安装命令`POSIXLY_CORRECT=1 sudo port install gmake libsdl git gnupg`；参见“参考链接-7”<br/>

&emsp;&emsp;3_1、安装jdk、下载repo、下载源码三个步骤，源码下载完成如果不再有`repo sync`的需求，可以删除.repo目录，参见`http://www.jianshu.com/p/1c3d47b2031f`<br/>

&emsp;&emsp;3_2、自动下载脚本,失败自动重试，注意：拷贝的时候如果第一个字符是斜杠，需要去掉！！！！
<pre>
\#!/bin/bash
repo sync  -j16
while [ $? = 1 ]; do  
        echo “======sync failed, re-sync again======”  
        sleep 3  
        repo sync  -j16
done
</pre>
<br/>

&emsp;&emsp;4、下载编译镜像对应的驱动，下载地址：`https://developers.google.com/android/drivers#hammerheadkot49h`，下载完成后解压到**源码根目录**得到两个或三个sh文件，然后执行，命令：`./extract-xxxx.sh`，执行之后会生成verdor目录，用于生成vendor.img<br/>

&emsp;&emsp;5、兼容处理，打开`build/core/combo/mac_version.mk`，查看变量`mac_sdk_versions_supported`所包含的版本，并下载所有版本，此处存放在~/Documents/configure/目录下，并在目录`/Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs`下创建链接，命令：`sudo ln -s ~/Documents/configure/MacOSX10.11.sdk /Applications/XCode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.11.sdk`<br/>

&emsp;&emsp;6、切换成bash，查看当前Shell命令：`echo $SHELL`，切换Shell命令`chsh -s /bin/zsh`；查看当前系统已安装的所有Shell`cat /etc/shells`<br/>

&emsp;&emsp;7、在源码根目录下执行命令：`source build/envsetup.sh`<br/>

&emsp;&emsp;8、输入命令`lunch`，并选择需要编译的版本，参考：`https://source.android.com/source/running.html#selecting-device-build`<br/>

&emsp;&emsp;8_1、BUILD TYPE介绍，参考`https://www.jianshu.com/p/9605f895d153`，`https://blog.csdn.net/netwalk/article/details/17383121`

&emsp;&emsp;9、执行编译命令：`make -jN`,N代表线程数，可以为4、8或16。

&emsp;&emsp;&emsp;&emsp;**注意：**1、如果想要删除创建的逻辑分区，只需要删除对应的dmg文件，并清空回收站即可！！！！

### 运行
&emsp;&emsp;**运行模拟器**，命令：`emulator`；<br/>
&emsp;&emsp;**真机运行** <br/>
&emsp;&emsp;1、进入目标目录：`cd $AOSP_HOME/out/target/product/angler` <br/>
&emsp;&emsp;2、使手机进入 fastboot 模式；命令：`adb reboot bootloader` 或手动进入，Nexus 6p是同时按住电源键和音量减键 <br/>
&emsp;&emsp;3、刷入img即可，命令`fastboot flashall -w` -w是清除/data分区，参考：`https://tuzhao.org/article/40` <br/>
&emsp;&emsp;4、安装谷歌相关服务，参考：`http://blog.csdn.net/fuchaosz/article/details/52473660`

### 导入Android Studio
&emsp;&emsp;0、此处需要先编译成功<br/>
&emsp;&emsp;1、`mmm development/tools/idegen/`，若mmm命令不存在则再次执行`source build/envsetup.sh`<br/>
&emsp;&emsp;2、`development/tools/idegen/idegen.sh`<br/>
&emsp;&emsp;3、使用Android studio打开任意一个项目，然后选择File->Open，打开根目录下的android.ipr文件夹，然后等待漫长的index完成后，就可以方便查看源码了。 **参见：参考链接2**<br/>
&emsp;&emsp;4、导入后的处理，参见：`http://blog.csdn.net/yanbober/article/details/48846331`

### Android Studio 中调试源码
&emsp;&emsp;1、 <br/>
**参考链接：** <br/>
&emsp;&emsp;1、自己动手调试Android源码：`http://blog.csdn.net/dd864140130/article/details/51815253` <br/>
&emsp;&emsp;2、Android Studio中调试Android源码：`http://blog.csdn.net/murphykwu/article/details/52117907` <br/>

### 常见问题
&emsp;&emsp;&emsp;&emsp;1、解决macOSX10.12.SDK下编译Android Open Source Project出错的问题（sycall过时）：http://palanceli.com/2016/09/25/2016/0925AOSPOnMac/<br/>

&emsp;&emsp;&emsp;&emsp;2、编译OOM：`http://blog.csdn.net/fengxingzhe001/article/details/78054827`

&emsp;&emsp;&emsp;&emsp;3、```java
build/core/config.mk:608: *** Error: could not find jdk tools.jar 
at /System/Library/Frameworks/JavaVM.framework/Versions/Current/Commands/../lib/tools.jar, 
please check if your JDK was installed correctly.  Stop.
```
**解决方案：** `$ export ANDROID_JAVA_HOME=$(/usr/libexec/java_home -v 1.7)` 

&emsp;&emsp;&emsp;&emsp;4、执行驱动.sh文件，无法生成vendor目录

&emsp;&emsp;&emsp;&emsp;5、如何查看当前分支的android版本及对应编号：<br/>
**1.**Android源码已全编译过，在build.prop(out/target/product/XXX/system/build.prop)里面查看ro.build.version.release的值<br/>
**2.**build/core/version_defaults.mk //搜索该文件中的PLATFORM_VERSION值

### 参考链接
&emsp;&emsp;&emsp;&emsp;0、**(重要)MAC下安装多版本JDK和切换几种方式**：http://chessman-126-com.iteye.com/blog/2162466 <br/>

&emsp;&emsp;&emsp;&emsp;1、常见问题：http://www.liball.me/mac-10-10-build-android-4-4-4-for-nexus/

&emsp;&emsp;&emsp;&emsp;2、(**参考**)Android源码的下载、编译与导入到Android Studio：http://wl9739.github.io/2016/05/09/Android%E6%BA%90%E7%A0%81%E7%9A%84%E4%B8%8B%E8%BD%BD%E3%80%81%E7%BC%96%E8%AF%91%E4%B8%8E%E5%AF%BC%E5%85%A5%E5%88%B0Android-Studio/

&emsp;&emsp;&emsp;&emsp;3、(**参考**)
mac系统android编译源码：`http://szysky.com/2016/07/12/mac%E7%B3%BB%E7%BB%9Fandroid%E7%BC%96%E8%AF%91%E6%BA%90%E7%A0%81/`;
Mac上下载编译Android 6.0源代码详细教程：`http://blog.csdn.net/yishon_android/article/details/51726676`
下载android 6.0源码、编译并刷入nexus 6p手机：`http://blog.csdn.net/fuchaosz/article/details/52473660`

&emsp;&emsp;&emsp;&emsp;4、Mac环境下Android源代码编译
：http://www.jianshu.com/p/ede53d42334d

&emsp;&emsp;&emsp;&emsp;5、macOS Sierra 编译android7.1源码：http://www.jianshu.com/p/8eab34f3a0aa

&emsp;&emsp;&emsp;&emsp;6、！！通过Xcode命令行编译：http://www.jianshu.com/p/55b80e746e38

&emsp;&emsp;&emsp;&emsp;7、macOS（Sierra 10.12）上Android源码（AOSP）的下载、编译与导入到Android Studio：`http://blog.bihe0832.com/macOS-AOSP.html`
