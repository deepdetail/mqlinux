## MQLinux - MoreQucik Linux OS for Router/Server

MQLinux ARM-Router Firmware for BPI-R1 & BPI-R2 Produced by [http://www.banana-pi.org/](http://www.banana-pi.org)

### ChangeLog

```
2019.04.01 19.02 Beta4
Update: Add mmc flash tools, One-click burning mmc flash in web (System->Disk Stoarge -> Burn Flash)

2019.03.29 19.02 Beta3
Update: Improve cloud management docking, support upgrade, restart, turn/off function
Update: Fix lang error for some pages

2019.03.22 19.02 Beta2
* many bugfix for UI & language error in translation

2019.03.18 frist release 19.02 Beta1
```

### Release notes

This is just the beta release, this firmware is totally free for personal use. 

Main  features:

* Kernel version: 4.9.44
* Highly streamlined embedded design system, running in memory
* Mutilple Language (en/zh_CN currently)
* DNS Proxy/Cache
* DDNS
* VLAN Extension for WAN
* Multiple WAN (each ethernet port can be defined)
* DHCP Server
* FTP Server
* PPPoE Server
* Samber Server
* VPN client/Server (PPTP VPN, IPsecVPN, OpenVPN)
* Cloud Login
* Firewall 
* IP-MAC Locking
* Port Mapping/DMZ/UPnP
* Diagnose Tools
* LVM/RAID support
...


here is a demo for cloud login: [https://bpi-r2.morequick.cn:84](https://bpi-r2.morequick.cn:84/)

username/passwd: demo/demo

![image](https://user-images.githubusercontent.com/16576843/54505845-b6000780-4974-11e9-80e4-dce4a262c815.png)

### Default parameters

1. The default username/password for webadmin & ssh login are admin/admin

2. The default port defination for BPI-R2 is WAN-LAN-LAN-LAN-LAN,  BPI-R1 is LAN-LAN-LAN-LAN-WAN

3. The default IP address for LAN is 192.168.1.254

4. The console login for TTL has no password


### TODO

1. On board WIFI module support
   
2. External USB, 4G module support
   
3. flash image to internal eMMC storage (Done at 2019/04/01)

Any advice and suggestions will be greatly appreciated,  Always happy to hear from your feedback. 

my email is emufly@gmail.com

### Download Image Link

via [GitHub](https://github.com/deepdetail/mqlinux/tree/master/files) or Google Drive bellow:

Updated at 2019/04/01 19.02 Beta4

>> For BPI-R2:

Google drive: https://drive.google.com/file/d/1NLUZQG7APUORvb-TUDNUtqYYR6cU92mf/view?usp=sharing

MD5 sum: 699583d11f7243420180dea5cd16ff32

>> For BPI-R1:

Google drive: https://drive.google.com/file/d/1TkvPcEZ4avxyOT7sFVo1xJOzMGTi8nKl/view?usp=sharing

MD5 sum: 9e44fd122be1e92bd08d600dd0b8483e
	

### Installation

1. Download the img.gz file, then unpack it, you will get MQLinux-ARM-19.02Beta1.for-mtk-bpi-r2-SD.img file

2. Prepare a TF card with a capacity greater than 256M, and a USB card reader

3.  We use [Balena Etcher](https://www.balena.io/etcher/) to flash the img to tfcard

   ![image](https://user-images.githubusercontent.com/16576843/54505758-3bcf8300-4974-11e9-9733-b07523993d88.png)
   
   For developer of Linux/macOS, u can just use dd command (be careful):

   macOS:
      sudo dd if=xxx.img of=/dev/<disk name, eg: sda,sdb,...> bs=1M

   Linux:
      sudo dd if=xxx.img of=/dev/<disk_id,eg: disk2,disk3,...> bs=1m


4. Put the tfcard into BPI-R2, hold the power key for at least 6 seconds

5. Wait about 1 minute or so the system will start up. then Connect the network cable to the second network port.

   ![IMG_3044](https://user-images.githubusercontent.com/16576843/54506419-50614a80-4977-11e9-9de0-3322c382bbfd.JPG)

6. visit the webUI for MQLinux, the URL is http://192.168.1.254/, username/passwd is both admin

### Burn firmware into built-in Flash

   Note: support BPI-R2 only, BPI-R1 do not have built-in storage

   webUI -> System -> Disk Storage, Burn Firmware 
   
   ![burnfm](https://user-images.githubusercontent.com/16576843/55299540-00e64880-5466-11e9-980f-ba7ea5376c65.png)
   
   ![burnfm_ok](https://user-images.githubusercontent.com/16576843/55299585-2bd09c80-5466-11e9-836b-fd818e181957.png)

After the operation is successful, shutdown, unplug the TF card, and then power on again.
