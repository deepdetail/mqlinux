## MQLinux for ARM

MQLinux ARM-Router Firmware for 

* BPI-R1 & BPI-R2 Produced by [http://www.banana-pi.org/](http://www.banana-pi.org)
* friendlyarm Nano Pi R2S

### ChangeLog

```
2020.06.08 1.2.2 Stable
Please visit https://docs.mqrouter.com/changelog.html

2020.04.24 1.2 Stable
Update: Supporrt Nano Pi R2S
Update: A lot bugfix & improve

2019.05.07 19.02 RC7
Update: Fix missing source IP for L2TP client link
Bugfix: Fix yunlogin ID maybe changed to randstr in some condition
Bugfix: internet ip for wan maybe incorrect sometimes
Bugfix: yunmgr upgrade cmd got unexp error msg
Update: add QCA9882/AR928X/AR5B91 mini-PCI-E WIFI module support for BPI-R2
Bugfix: sslvpn client cannot connect to server due to file permission

2019.04.01 19.02 Beta4
Update: Add mmc flash tools, One-click burning mmc flash in web (System->Disk Stoarge -> Burn Flash)

2019.03.29 19.02 Beta3
Update: Improve cloud management docking, support upgrade, restart, turn/off function
Update: Fix lang error for some pages

2019.03.22 19.02 Beta2
* many bugfix for UI & language error in translation

2019.03.18 first release 19.02 Beta1
```

### Release notes

This firmware is totally free for all purpose use. 

Main  features:

* Kernel version: 4.9.44
* Highly streamlined embedded design system, running in memory
* Multiple Language (en/zh_CN currently)
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
* external WIFI module support（QCA9882/AR928X/AR5B91)
...

![image](https://user-images.githubusercontent.com/16576843/54505845-b6000780-4974-11e9-80e4-dce4a262c815.png)

### Default parameters

1. The default username/password for webadmin & ssh login are admin/admin

2. The default port defination for BPI-R2 is WAN-LAN-LAN-LAN-LAN,  BPI-R1 is LAN-LAN-LAN-LAN-WAN

3. The default IP address for LAN is 192.168.1.254

4. The console login for TTL has no password


### TODO

1. On board WIFI module support （not support, please use external mpci-e module)
   
2. External USB, 4G module support
   
3. flash image to internal eMMC storage (Done at 2019/04/01)

Any advice and suggestions will be greatly appreciated,  Always happy to hear from your feedback. 

my email is emufly@gmail.com

### Installation

1. Download the img.gz file, then unpack it, you will get MQLinux-ARM-19.02Beta1.for-mtk-bpi-r2-SD.img file

2. Prepare a TF card with a capacity greater than 256M, and a USB card reader

3.  We use [Balena Etcher](https://www.balena.io/etcher/) to flash the img to tfcard

   ![image](https://user-images.githubusercontent.com/16576843/54505758-3bcf8300-4974-11e9-9733-b07523993d88.png)
   
   For developer of Linux/macOS, u can just use dd command (be careful):

   macOS:
      sudo dd if=xxx.img of=/dev/<disk_id,eg: disk2,disk3,...> bs=1m

   Linux:
      sudo dd if=xxx.img of=/dev/<disk name, eg: sda,sdb,...> bs=1M


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
