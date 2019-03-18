## MQLinux - MoreQucik Linux OS for Router/Server

MQLinux ARM 19.02beta1 Router for BPI-R2

### Release notes

This is the first beta release , this firmware is totally free for personal use. 

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
...


here is a demo for cloud login: [https://bpi-r2.morequick.cn:84](https://bpi-r2.morequick.cn:84/)

username/passwd: demo/demo

### Default parameters

1. The default username/password for webadmin & ssh login are admin/admin

2. The default port defination is WAN-LAN-LAN-LAN-LAN

3. The default IP address for LAN is 192.168.1.254

4. The console login for HDMI/TTL has no password


### TODO

1. On board WIFI module support
   
2. External USB, 4G module support
   
3. flash image to internal eMMC storage

Any advice and suggestions will be greatly appreciated,  Always happy to hear from your feedback. 

my email is emufly@gmail.com

### Download Image Link

Google drive:https://drive.google.com/file/d/1Ws2IUiCGSKKQ2dCM5XJBV-pog-hk17PM/view?usp=sharing

MD5 sum: 09b58f050166ed5d09803e1de56d7890

### Installation

1. Download the img.gz file, then unpack it, you will get MQLinux-ARM-19.02Beta1.for-mtk-bpi-r2-SD.img file

2. Prepare a TF card with a capacity greater than 256M, and a USB card reader

3.  We use [Balena Etcher](https://www.balena.io/etcher/) to flash the img to tfcard

4. Put the tfcard into BPI-R2, hold the power key for at least 6 seconds

5. Wait about 1 minute or so the system will start up. then Connect the network cable to the second network port.

6. visit the webUI for MQLinux, the URL is http://192.168.1.254/, username/passwd is both admin