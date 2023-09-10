# W600-TB01
源代码来自： [Huii-Wang/W600-TB01](https://github.com/Huii-Wang/W600-TB01),
>备注：W600踩坑记录  绿联WIFI模块 无线收发模块 阿里云iOT AliOS-Things

## 官方介绍[W600——新一代嵌入式 Wi-Fi SoC 芯片](https://www.winnermicro.com/html/1/156/158/497.html)
### 1. 产品介绍

>W600 芯片是一款支持多接口、多协议的无线局域网IEEE802.11n（1T1R）的SoC芯片。适用于智能家电、智能家居、无线音视频、智能玩具、医疗监护、工业控制等物联网应用领域。该SoC芯片集成Cortex-M3内核，内置Flash，集成射频收发前端RF Transceiver，CMOS PA功率放大器，基带处理器/媒体访问控制，支持SDIO、SPI、UART、GPIO、I²C、PWM、I²S、7816等接口, 支持多种加解密协议，如PRNG/SHA1/MD5/RC4/DES/3DES/AES/CRC/RSA等。

### 2. 详细规格
芯片功能框图
![img](https://cdn.nlark.com/yuque/0/2023/png/35335856/1694349586217-aefb5239-2aa8-44b2-aaef-38c48db0b164.png)

### 3.芯片封装介绍：

QFN32

![img](https://cdn.nlark.com/yuque/0/2023/jpeg/35335856/1694349586239-8ab1bbd2-20c1-4109-94ee-0616e6bf5e89.jpeg)

### 4.规格介绍：  

#### 4.1 芯片集成度
- 集成32位嵌入式Cortex-M3处理器，工作频率80MHz；
- 集成288KB数据存储器；
- 集成1MB FLASH；
- 集成2.4G射频收发器，满足IEEE802.11规范；
- 集成PA/LNA/TR-Switch；
- 集成32.768KHz时钟振荡器；
- 集成电源管理电路；
- 集成通用加密硬件加速器，支持PRNG/SHA1/MD5/RC4/DES/3DES/AES/CRC/RSA等多种加解密协议；

####  4.2 芯片接口：
- 1 x SDIO2.0 Deviece接口
- 2 x UART，38Kbps~2Mbps
- 1 x 高速SPI，最高50Mbps
- I²C
- PWM
- I²S
- GPIO



#### 4.3 Wi-Fi协议与功能 
- IEEE802.11b/g/n
- WAPI2.0
- Wi-Fi WMM/WMM-PS/WPA/WPA2/WPS
- Wi-Fi Directo
- 支持20/40M带宽工作模式
- 支持STA/AP/AP+STA模式



## 调试记录
[W600-TB01调试文档](W600-TB01/README.md)
[正点原子开发板调试文档](W601_IoT_Board-1.0.2/README.md)