##ReactNative教程##
---关键字--- ReactNative

###运行应用
#####在Android上运行app
```java
export ANDROID_HOME=/Users/KoreQ/Library/Android/sdk
cd android
./gradlew installDebug
adb reverse tcp:8081 tcp:8081   // 使用 adb 端口代理，确保设备可以访问 Packager 和 GraphQL server
adb reverse tcp:8080 tcp:8080
```


###遇到问题
&emsp;&emsp;1、使用`npm install`报错，可以在终端输入命令来配置代理（只对当前终端生效）
`export http_proxy="http://127.0.0.1:1080"`
`export https_proxy="http://127.0.0.1:1080"`

&emsp;&emsp;**解决方案**

&emsp;&emsp;&emsp;&emsp;1、（推荐）npm用法以及更换到淘宝镜像的方法
：http://blog.csdn.net/zhangwenwu2/article/details/52778521

&emsp;&emsp;&emsp;&emsp;2、配置终端代理的多种方法：
：https://blog.fazero.me/2015/09/15/%E8%AE%A9%E7%BB%88%E7%AB%AF%E8%B5%B0%E4%BB%A3%E7%90%86%E7%9A%84%E5%87%A0%E7%A7%8D%E6%96%B9%E6%B3%95/

&emsp;&emsp;&emsp;&emsp;3、使用proxychains配置终端代理：
：http://gaocegege.com/Blog/%E9%9A%8F%E7%AC%94/shadowsocks-with-terminal

&emsp;&emsp;&emsp;&emsp;4、使用polipo配置终端代理：http://droidyue.com/blog/2016/04/04/set-shadowsocks-proxy-for-terminal/index.html


###参考链接

&emsp;&emsp;&emsp;&emsp;1、RN学习指南-汇集各类学习资源
：https://github.com/reactnativecn/react-native-guide、https://github.com/jondot/awesome-react-native

&emsp;&emsp;&emsp;&emsp;2、F8APP-源码
：https://github.com/fbsamples/f8app

&emsp;&emsp;&emsp;&emsp;3、F8APP学习教程
：https://f8-app.liaohuqiu.net/#content

&emsp;&emsp;&emsp;&emsp;4、Exemplary RN apps
：https://rnplay.org/apps/picks

&emsp;&emsp;&emsp;&emsp;5、Node.js安装和简易服务器配置：http://neikvon.blog.51cto.com/4266757/1155998

&emsp;&emsp;&emsp;&emsp;6、Mac下安装MongoDB 及使用教程:
https://segmentfault.com/a/1190000002547229

&emsp;&emsp;&emsp;&emsp;7、Xcode快捷键:
http://www.jianshu.com/p/19f2e25afa65
