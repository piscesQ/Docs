## Android Studio 中 NDK 开发##
---关键字--- Android Studio NDK

### 环境
AS2.3

NDK-r15

### 官方网站
&emsp;&emsp;NDK下载：http://developer.android.com/ndk/downloads/index.html#download

官网：https://developer.android.com/ndk/index.html?hl=zh-cn

官网示例：https://developer.android.com/ndk/samples/index.html?hl=zh-cn

github源码：https://github.com/googlesamples/android-ndk


### 开发流程
&emsp;&emsp;1、创建工程，并创建一个类，此处类名为：NativeUtils，并在类中声明一个“native”的抽象方法；

&emsp;&emsp;2、使用“javac”命令生成class文件，再使用“javah”命令生成.h文件

&emsp;&emsp;3、将生成的.h文件拷入src/main/jni目录，再新建一个cpp文件，并实现.h文件中的方法

&emsp;&emsp;4、在jni目录下添加Android.mk和Application.mk，具体见“参考链接-2”

&emsp;&emsp;5、在目录jni下打开命令行，执行命令“ndk-build”，即可生成对应so文件

&emsp;&emsp;6、将生成的so文件拷入src/main/jniLibs目录即可

&emsp;&emsp;7、然后在使用native方法之前loadLibrary即可，此处可以在NativeUtils中的静态代码块加载so库

#### 打印Log
&emsp;&emsp;**NDK开发之日志打印**：https://blog.csdn.net/u012702547/article/details/48222859

#### JNI调用java静态和成员方法
**JNI/NDK开发指南（六）——C/C++访问Java实例方法和静态方法**：https://blog.csdn.net/xyang81/article/details/42582213

### 未解决问题
&emsp;&emsp;1、直接运行时会报错：找不到对应的库，打成so包之后可以正常运行
&emsp;&emsp;2、两个jstring拼接后作为返回值返回，曲线救国：可都转成char*然后再拼接，最后再使用NewStringUTF转成jstring

&emsp;&emsp;3、jni回调方法内部为什么不能直接更新UI？回调方法运行在主线程，为什么不能呢？

### 常见问题
&emsp;&emsp;1、**Android NDK: Aborting出现NDK_PROJECT_PATH=null解决方法**：https://www.jianshu.com/p/4fd207f27bfb

&emsp;&emsp;2、**ISO C++11 does not allow conversion from string literal to 'char *'**：https://www.jianshu.com/p/a0b3d2a263fb

### 参考链接
&emsp;&emsp;&emsp;&emsp;1、**使用Android Studio 进行NDK开发和调试**：https://www.jianshu.com/p/2690c9964110 <br/>

&emsp;&emsp;&emsp;&emsp;2、**Android Studio jni开发入门——看我就够了！**：http://www.jcodecraeer.com/a/anzhuokaifa/2017/0401/7769.html

&emsp;&emsp;&emsp;&emsp;3、**Android NDK 教程 - NDK环境配置和 Android Studio 中的入门使用**：https://blog.csdn.net/piscesq329a/article/details/50113463

&emsp;&emsp;&emsp;&emsp;4、**JNI中string 、 char* 和 jstring 两种转换**：https://blog.csdn.net/xlxxcc/article/details/51106721