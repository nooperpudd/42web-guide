
# 大屏幕方案

## 屏幕结构

屏幕尺寸：`704*1632`


屏幕分配比例:
* 上方屏幕：`1252*704`
* 中间：`704*120`
* 底部：`704*260`


## 安装配置

### 控制系统

1. 控制屏幕开关
2. 控制播放方案
3. 控制PLC系统


### 播放系统

需要安装精显时代播放方案。

##### Tips - 解决IE下的bug

测试IE版本：http://www.iefans.net/wp-demo/ie.html

需要对注册表进行修改。

需要解决Web播放IE内核下的bug:

具体参考：
1. [强制使用IE版本](http://www.cnblogs.com/zhwl/p/3147832.html)

2. [IE内核版本号](
    http://zhidao.baidu.com/link?url=Uruz3Xs9bjmNz5FCBALwGg2ZGjTAWsQWhvmOMEiHG8wGTMCepmQC6EXqApsMpFjhh7W0VWQGeH2duiuoGlHHVy1X07ISXTduI3jNkIPP7jq)

### Docker 虚拟机
需要安装docker 虚拟机

如何启动docker 虚拟器：

    1.  首先启动virtual box.
    2.  然后启动xshell登陆docker虚拟器。

在xshell中启动启动虚机。

    $ docker start -i lastscreen

启动：

    $ service nginx start
    $ service mysql start
    $ /opt/tianshihui/tools/lanuch.sh start

重新启动：

    $ service /opt/tianshihui/tools/lanuch.sh restart

更新代码：

    $ /opt/tinashihui/tools/export.sh master

本机访问地址：

    http://bigscreen.angelcrunch.com



#### 开启远程服务功能

启动：

    $service ssh start

    $autossh -M 5678 -N -R 12306:localhost:22 root@119.254.111.196

    $ssh -Nf -R 12306:localhost:22 root@119.254.111.196

    $autossh -M 3442 -R -N 4000:localhost:80 root@119.254.111.196

### 字体库程序

需要安装字体库方案。


### Windows 配置

1. Windows 必须禁用休眠和待机功能。
2. Windows 最好开启系统还原功能。
3. 修改hosts配置，增加`bigscreen.angelcrunch.com 127.0.0.1`.



# 播放器功能

### 播放器方案：
通过精显时代可以控制分屏播放方案。

播放器分成三个屏幕：
* 上方屏幕播放主显示内容。
* 中间播放滚动条功能。
* 底部保留logo。

###  Web 后台管理程序

* web地址： bigscreen.angelcrunch.com/admin
* 后台用户： admin@angelcrunch.com
* 密码：单独联系。
* 后台目录：http://bigscreen.angelcrunch.com:8080


###  AirPay 

需要提供单独的路由器，首先要检测路由器的信道是不是处于干扰频段，尽量保证高质量的传输过程中，应当使用单独的信道进行。

Apple TV 播放：
通过Iphone AirPay 功能。

Android 播放：
小米采用mirror cast播放功能并不能够很好的支持IOS设备。
通过小米黑子播放。








