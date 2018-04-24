##Linux安装Tomcat##
---关键字--- tomcat jdk

###环境
&emsp;&emsp;&emsp;&emsp;CentOS 6.8 命令行

###安装JDK
&emsp;&emsp;&emsp;&emsp;1、下载jdk，使用`wget`命令：`wget http://120.52.72.22/download.oracle.com/c3pr90ntc0td/otn-pub/java/jdk/8u121-b13/e9e7ea248e2c4826b92b3f075a80e441/jdk-8u121-linux-x64.tar.gz`（2017年0306最新版本）<br/>
&emsp;&emsp;&emsp;&emsp;2、解压，命令：`tar zxvf jdk-8u121-linux-x64.tar.gz`<br/>
&emsp;&emsp;&emsp;&emsp;3、添加环境变量，将环境变量放入`/etc/profile`文件中，添加内容如下：<br/>
```java
  JAVA_HOME=/root/dev/jdk1.8.0_121
  JRE_HOME=$JAVA_HOME/jre
  PATH=$PATH:$JAVA_HOME/bin
  CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
  export JAVA_HOME
  export JRE_HOME
  export PATH
  export CLASSPATH
```
&emsp;&emsp;&emsp;&emsp;4、使用命令`java -version`进行测试<br/>


###参考链接
&emsp;&emsp;&emsp;&emsp;1、十款最常见的Linux发行版及目标用户：`http://os.51cto.com/art/201307/404309_all.htm`<br/>

&emsp;&emsp;&emsp;&emsp;2、Linux命令行安装JDK 安装：`http://wiki.jikexueyuan.com/project/linux-in-eye-of-java/JDK-Install.html`




