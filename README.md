# W600-TB01
绿联WIFI模块 无线收发模块 阿里云iOT

## 踩坑记录
    淘宝买的5.9的模块直接用接线比较麻烦，后来直接买了9.9的W600开发板，调试非常方便

## 资料收集
    联盛德 资料 https://docs.w600.fun
    官网资料 http://www.winnermicro.com/html/1/156/158/497.html?tdsourcetag=s_pcqq_aiomsg
    开发板TB-01提供资料：Github源码：https://github.com/w600
    官网网站：https://www.w600.fun
    问答社区：https://ask.w600.fun
    文档中心：https://docs.w600.fun
    下载中心：https://download.w600.fun



## 兼容ESP8266 AT固件
    https://docs.w600.fun/?p=at/esp-start.md





## Arduino SDK 

## RT-Thread SDK
## AliOS Things SDK
### 编译非常方便，文档写的也不错
#### 踩坑记录
    刚开始使用时候，编译不过，发现是一个编译工具无法下载，原因是该工具上传到码云，下载需要登录和验证码，手动下载配置后，编译通过。
    
    目前在使用配网信息时候，需要使用阿里智能生活的APP，免开发模式挺好用。但是考虑到后续授权码要收费的问题，就没有继续研究

## 联盛德官方SDK
### 根据文档可以分为以下几个SDK：
        WM_AT固件
        SPI透传固件
        Soc二次开发固件 这个资料和功能比较全，打算使用这一套进行开发


#### 配网模式

    量产时候需要注意天线的强度，2.4G路由器在我右侧，把目标板放到我的左侧就不可以连接，右侧就可以进行连接

    http://docs.thingsturn.com/download/soc/#id2
    根据连接中的 W60X_SDK使用手册，配网模式使用如下

    t-connect("Lenze","Lenze888888")     这个比较好用，基本每次连接都成功

    t-oneshot 一键配网模式 连接2.4G的网络成功率高一些，注意连接的是目标网络，不是设备网络

    airkiss 配网 和一键配网模式差不多，2.4G的成功率很高，5G的偶尔才可以连接上

    t-webcfg 配网 使用也很方便，连接上设备wifi SoftAp后，进入192.168.1.1进行网络设置    
        
#### SOCKET链接
    这里不过多介绍SOCKET。SOCKET连接类似管道连接。
    使用SOCKET首先要有一个服务器，一个客户端，进行双向通讯。SOCKET的特点是及时性高，缺点是消耗资源。

    根据官方资料进行下载 NetAssist，创建一个TCP Server,端口号为8080

    t-sockc(8080,192.168.1.198)
    注意：要杀掉360 网络调试助手要注意是TCP还是UDP

    UDP单播和UDP多播和此操作类似

    DEMO_APSTA


#### http Demo
    项目中有一个报错，无法编译，原因是 RemoteIp重名。把其中一个RemoteIp改命名即可。
    t-httpfwup=(http://192.168.1.198/W600/WM_W600_GZ.img)
    t-httpgetLocation: http://192.168.1.100:8080/TestWeb/
