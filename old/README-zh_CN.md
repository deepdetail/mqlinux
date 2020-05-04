## MQLinux  - 适用于路由器/服务器的MoreQuick Linux操作系统

用于[http://www.banana-pi.org/](http://www.banana-pi.org）出品的 BPI-R1和BPI-R2的MQLinux ARM-Router固件

### 更新日志

```
2019.04.01 19.02 Beta4
Update: 添加mmc闪存工具，在Web上一键烧录当前运行的固件到内置MMC存储（系统->磁盘存储->烧录固件）

2019.03.29 19.02 Beta3
Update: 改进云管理对接，支持升级，重启，关闭/关闭功能
Update: 修复某些页面的语言错误

2019.03.22 19.02 Beta2
Update: 修复许多UI及翻译中的语言错误

2019.03.18 初次发布19.02 Beta1
```

### 发行说明

这个固件完全免费供非商业使用。

主要特点：

* 内核版本：4.9.44
* 高度简化的嵌入式设计系统，在内存中运行
* 多语言支持（目前为en / zh_CN）
* DNS代理/缓存
* DDNS
* WAN的VLAN扩展
* 多个WAN（可定义每个以太网端口）
* DHCP服务器
* FTP服务器
* PPPoE服务器
* Samber服务器
* VPN客户端/服务器（PPTP VPN，IPsecVPN，OpenVPN）
* 云登录
* 防火墙
* IP-MAC锁定
* 端口映射/ DMZ / UPnP
* 诊断工具
* LVM / RAID支持
...

云登录演示：[https://bpi-r2.morequick.cn:84](https://bpi-r2.morequick.cn:84/)

用户名/密码: demo/demo

![image](https://user-images.githubusercontent.com/16576843/54505845-b6000780-4974-11e9-80e4-dce4a262c815.png)

### 默认参数

1. webadmin和ssh登录的默认用户名/密码是admin / admin

2. BPI-R2的默认网口定义是WAN-LAN-LAN-LAN-LAN，BPI-R1是LAN-LAN-LAN-LAN-WAN

3. LAN的默认IP地址是192.168.1.254

4. TTL的控制台登录没有密码


### TODO

1. 板载WIFI模块支持
   
2. 外置USB，4G模块支持
   
3. 闪存映像到内部eMMC存储（已完成于2019/04/01）

任何建议和建议将不胜感激，总是很高兴收到您的反馈意见, 我的电子邮件是emufly@gmail.com

### 镜像下载链接

通过[GitHub](https://github.com/deepdetail/mqlinux/tree/master/files) 或Google Drive：

更新于2019/04/01 19.02 Beta4

>用于BPI-R2：

Google云端硬盘：https：//drive.google.com/file/d/1NLUZQG7APUORvb-TUDNUtqYYR6cU92mf/view?usp=sharing

MD5校验：699583d11f7243420180dea5cd16ff32

>用于BPI-R1：

Google云端硬盘：https：//drive.google.com/file/d/1TkvPcEZ4avxyOT7sFVo1xJOzMGTi8nKl/view?usp=sharing

MD5校验：9e44fd122be1e92bd08d600dd0b8483e


### 安装

1. 下载img.gz文件，然后将其解压缩，您将获得MQLinux-ARM-19.02Beta1.for-mtk-bpi-r2-SD.img文件

2. 准备容量大于256M的TF卡和USB读卡器

3. 我们使用[Balena Etcher]（https://www.balena.io/etcher/）将img克隆到TF卡

   ![image](https://user-images.githubusercontent.com/16576843/54505758-3bcf8300-4974-11e9-9733-b07523993d88.png)
   
   对于Linux / macOS的开发人员，你可以使用dd命令（小心）：

   苹果系统：
      sudo dd if=xxx.img of=/dev/<disk_id，例如：disk2，disk3，...> bs=1m

   Linux系统：
      sudo dd if=xxx.img of=/dev/<磁盘名称，例如：sda，sdb，...> bs=1M


4. 将tf卡插入BPI-R2，按住电源键至少6秒钟

5. 等待大约1分钟左右，系统将启动。然后将网络电缆连接到第二个网络端口。

   ![IMG_3044](https://user-images.githubusercontent.com/16576843/54506419-50614a80-4977-11e9-9de0-3322c382bbfd.JPG)

6. 访问webUI for MQLinux，URL为 http://192.168.1.254/, 默认账号和密码均为 admin

### 将固件烧录到内置Flash中

   注意：仅支持BPI-R2，BPI-R1没有内置存储

   webUI  ->系统 ->磁盘存储，烧录固件
   
   ![burnfm](https://user-images.githubusercontent.com/16576843/55299540-00e64880-5466-11e9-980f-ba7ea5376c65.png)
   
   ![burnfm_ok](https://user-images.githubusercontent.com/16576843/55299585-2bd09c80-5466-11e9-836b-fd818e181957.png)

操作成功后，关机，拔下TF卡，然后重新打开电源。
