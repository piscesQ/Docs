##直播教程##
---关键字--- SRS配置

###SRS的配置
#####相关文件
&emsp;&emsp;&emsp;&emsp;1、源码地址：https://github.com/ossrs/srs<br/>
&emsp;&emsp;&emsp;&emsp;2、**官网教程**：https://github.com/ossrs/srs/wiki/v2_CN_Home <br/>
&emsp;&emsp;&emsp;&emsp;3、参考 - simple-rtmp-server教程：http://www.yiibai.com/t/simple-rtmp-server <br/>
&emsp;&emsp;&emsp;&emsp;**！注意：**：在mac上执行`./configure`时一定要带上`--osx`参数！！！

#####Demo配置步骤
&emsp;&emsp;&emsp;&emsp;1、Demo配置文档：`https://github.com/ossrs/srs/wiki/v1_CN_SampleDemo` <br/>
&emsp;&emsp;&emsp;&emsp;2、上面文档中当执行：`bash scripts/build.sh`时，需要指定系统为`osx`，所以应使用命令`./configure --demo --osx && make`来代替文档中的命令。 <br/>
&emsp;&emsp;&emsp;&emsp;3、启动完成后，在终端会输出相应的调试网址，可以进行测试。 <br/>
&emsp;&emsp;&emsp;&emsp;4、同时，也可以使用官方调试网址
http://www.ossrs.net/players/srs_player.html# <br/>

#####SRS配置步骤
&emsp;&emsp;&emsp;&emsp;1、srs服务器启动：`https://github.com/ossrs/srs/tree/2.0release#usage` <br/>
&emsp;&emsp;&emsp;&emsp;2、部署RTMP：`https://github.com/ossrs/srs/wiki/v1_CN_SampleRTMP` <br/>
&emsp;&emsp;&emsp;&emsp;3、配置HLS（不使用nginx）：`https://github.com/ossrs/srs/wiki/v2_CN_SampleHTTP` <br/>
&emsp;&emsp;&emsp;&emsp;4、配置转码以及设置分辨率等： `https://github.com/ossrs/srs/wiki/v2_CN_FFMPEG`；<br/>
按照文档中“Transcode Confid”中的说明进行配置，观看转码流的地址应为：`rtmp://dev:1935/live/livestream_example`


#####SRS回调配置
&emsp;&emsp;&emsp;&emsp;1、<br/>
&emsp;&emsp;&emsp;&emsp;2、<br/>


###采集客户端

######OBS
&emsp;&emsp;&emsp;&emsp;1、下载地址：https://obsproject.com/download <br/>
&emsp;&emsp;&emsp;&emsp;2、配置教程 - 简书：http://www.jianshu.com/p/ecfaac6ee7ab

######FMLE下载和配置
&emsp;&emsp;&emsp;&emsp;1、如何配置Flash Media Live Encoder (FMLE)从而使用Azure直播服务：https://blogs.msdn.microsoft.com/azchina/2015/02/15/flash-media-live-encoder-fmleazure/ <br/>
&emsp;&emsp;&emsp;&emsp;2、使用 FMLE 编码器发送单比特率实时流：https://github.com/bingosummer/techcontent/blob/master/articles/media-services-configure-fmle-live-encoder.md <br/>
&emsp;&emsp;&emsp;&emsp;3、fmle使用指南：http://www.baofengcloud.com/cases/livefmle.html <br/>
&emsp;&emsp;&emsp;&emsp;**待解决问题：**FMLE在无法识别mac摄像头，无法使用该摄像头录制视频。


###参考链接

&emsp;&emsp;&emsp;&emsp;1、