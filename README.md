# crack
>端口服务爆破及目标扫描(兼容Debian、Centos、Ubuntu、Kali、Mint)
>声明:写这个脚本并无它意，只是为了简便安全测试人员，提升系统安全性，战场没有怜悯之心，你若捡起手中的武器，你将犯下滔天大错。
>用户使用该脚本所产生的法律后果自行承担，本站概不负责。

**`运行方式`**

_本地运行:_
```shell
git clone https://github.com/RokasUrbelis/crack.git 
cd crack
bash crack.sh
```

_curl运行:_
```shell
bash -c "$(curl -fsSl https://blog.linux-code.com/scripts/crack.sh)"
```

_docker镜像运行:_
```shell
docker run -ti --name crack sebastion/crack:1.0 crack.sh
```
***进入容器运行:***
```shell
docker run -ti -d --name crack1 sebastion/crack:1.0 /bin/bash
$ docker exec -ti $(awk '{FS="[ ]+"}{if(NR==2){print $1}}'< <(docker ps -l)) /bin/bash
$ bash crack.sh
```
***一次性容器运行:***
```bash
docker run --rm -ti sebastion/crack:1.0 /crack.sh
```
欢迎访问[我的博客](http://blog.linux-code.com "悬停显示"):blush:
