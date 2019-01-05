# system_safety_test
[![](https://img.shields.io/badge/nmap-7.7-blue.svg)](https://nmap.org)
[![](https://img.shields.io/badge/hydra-8.6-red.svg)](https://www.thc.org)
[![](https://img.shields.io/badge/docker-18.09-green.svg)](https://hub.docker.com)
[![](https://img.shields.io/badge/debian-support-orange.svg)](https://www.debian.org)
>支持端口服务爆破及目标扫描(兼容Debian、Centos、Ubuntu、Kali、Mint)
>>声明:写这个脚本并无它意，只是为了简便安全测试人员，提升系统安全性，战场没有怜悯之心，你若捡起手中的武器，你将犯下滔天大错。
>>用户使用该脚本所产生的法律后果自行承担，本站概不负责。
>>容器运行方式根目录自带`user.txt`和`password.txt`两个字典，同时git下也保存了用户名字典文件，你可以自定义字典使用

***支持两种爆破方式***
* nmap
  - [x] 1.服务及端口探测
  - [x] 2.操作系统识别
  - [x] 3.指定端口或端口范围扫描
  - [x] 4.漏洞扫描
  - [x] 5.WHOIS查询
  - [x] 6.探测指定网段所有在线主机
  - [x] 7.主机批量扫描
  - [x] 8.调用其它脚本扫描

* hydra
  - [x] 1.SSH爆破
  - [x]  2.Redesktop爆破
  - [x]  3.FTP爆破
  - [x]  4.Telnet爆破
  - [x]  5.MySql爆破
  - [x]  6.smb爆破
  - [x]  7.mssql爆破
  - [x]  8.其他协议爆破
  
>目前集成上去的协议有:
>>asterisk cvs cisco-enable firebird ftp ftps icq imap irc ldap2 nntp mssql
    mysql oracle-sid pcanywhere pcnfs pop3 rdp postgres radmin2  rexec rlogin rpcap rtsp 
    sip smb smtp smtp-enum socks5 ssh sshkey svn teamspeak vnc xmpp

## 运行方式

***本地运行:***
```shell
git clone https://github.com/RokasUrbelis/system_safety_test.git 
cd crack
bash crack.sh
```

***curl运行:***
```shell
bash -c "$(curl -fsSl https://blog.linux-code.com/scripts/crack.sh)"
```
***docker镜像运行:***
```shell
docker run -ti --name crack sebastion/crack:1.0 crack.sh
```
![](https://blog.linux-code.com/wp-content/uploads/2018/12/crack-show2.png)

***进入容器运行:***
```shell
docker run -ti -d --name crack1 sebastion/crack:1.0 /bin/bash
docker exec -ti $(awk '{FS="[ ]+"}{if(NR==2){print $1}}'< <(docker ps -l)) /bin/bash
bash crack.sh
```
![](https://blog.linux-code.com/wp-content/uploads/2018/12/docker-show.png)

***一次性容器运行:***
```shell
docker run --rm -ti sebastion/crack:1.0 /crack.sh
```
![](https://blog.linux-code.com/wp-content/uploads/2018/12/docker-show2-676x640.png)

***使用Dockerfile构建镜像并运行容器:***
```shell
git clone https://github.com/RokasUrbelis/system_safety_test.git
cd system_safety_test
docker build -t crack:1.0 .
docker run --ti --rm crack:1.0
```
## Follow Me
* Email: lonlyterminals@gmail.com
* QICQ ：1798996632
* 以及[我的博客](https://blog.linux-code.com "blog.linux-code.com"):blush:（可订阅本站RSS了解更多技术文章）
