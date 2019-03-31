# System security test
[![](https://img.shields.io/badge/nmap-7.7-blue.svg)](https://nmap.org)
[![](https://img.shields.io/badge/hydra-8.6-red.svg)](https://www.thc.org)
[![](https://img.shields.io/badge/Bash-Language-black.svg)](https://www.debian.org)
[![](https://img.shields.io/badge/docker-18.09-brightgreen.svg)](https://hub.docker.com)
[![](https://img.shields.io/badge/debian-support-orange.svg)](https://www.debian.org)
[![](https://img.shields.io/github/stars/Acoustroal/System-security-testing.svg?label=Stars&style=social)](https://github.com/Acoustroal/System-security-testing)
# Before this
- Support port service brute and target scanning (compatible with Debian/Centos/Ubuntu/Kali/Mint,if you use the docker container run the script,then compatible with all linux distros)

### Hereby certify:
- There is no purpose in writing this script, just for the convenience of security testers and improve system security, there is no mercy in the battlefield, if you pick up the hands of weapons, you will make a terrible mistake.
- The author is not responsible for any legal consequences arising out of the user's use of this script.
- Container operation mode the root directory of the cabin `user.txt` and `password.txt` two files, also you can use a custom dictionary by yourself

***The following two methods of security testing are supported***
* nmap
  - [x] 1.Service and port scanning
  - [x] 2.OS identification
  - [x] 3.Specifies a port or port range to scanning
  - [x] 4.Vulnerability scanning
  - [x] 5.WHOIS query
  - [x] 6.Probes all online hosts in a specified network segment
  - [x] 7.Host batch scanning
  - [x] 8.Call any nmap scripts to scanning

* hydra
  - [x]  1.SSH brute
  - [x]  2.Redesktop brute
  - [x]  3.FTP brute
  - [x]  4.Telnet brute
  - [x]  5.MySql brute
  - [x]  6.Smb brute
  - [x]  7.Mssql brute
  - [x]  8.Other protocol brute
  
>There are currently several supported protocols:
>>asterisk cvs cisco-enable firebird ftp ftps icq imap irc ldap2 nntp mssql
    mysql oracle-sid pcanywhere pcnfs pop3 rdp postgres radmin2  rexec rlogin rpcap rtsp 
    sip smb smtp smtp-enum socks5 ssh sshkey svn teamspeak vnc xmpp

# Run

***git:***
```shell
git clone https://github.com/RokasUrbelis/system_safety_test.git 
cd crack
bash crack.sh
```
***curl:***
```shell
bash -c "$(curl -fsSl https://blog.linux-code.com/scripts/crack.sh)"
```
***docker container:***
```shell
docker run -ti --name crack sebastion/crack:1.0 crack.sh
```
![](https://blog.linux-code.com/wp-content/uploads/2018/12/crack-show2.png)

***enter the container:***
```shell
docker run -ti -d --name crack1 sebastion/crack:1.0 /bin/bash
docker exec -ti $(awk '{FS="[ ]+"}{if(NR==2){print $1}}'< <(docker ps -l)) /bin/bash
bash crack.sh
```
![](https://blog.linux-code.com/wp-content/uploads/2018/12/docker-show.png)

***temporary container run:***
```shell
docker run --rm -ti sebastion/crack:1.0 /crack.sh
```
![](https://blog.linux-code.com/wp-content/uploads/2018/12/github-show2.png)

***Use Dockerfile to build the image and run the container:***
```shell
git clone https://github.com/RokasUrbelis/system_safety_test.git
cd system_safety_test
docker build -t crack:1.0 .
docker run --ti --rm crack:1.0
```
# Follow Me
* Email: Rokas.Yang@gmail.com
* QICQ ：1798996632
* And [Blog](https://blog.linux-code.com "blog.linux-code.com"):blush:（Subscribe to our RSS feed for more technical articles）
