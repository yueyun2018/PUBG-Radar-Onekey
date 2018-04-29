## 搭建加速器
```bash
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh

chmod +x shadowsocks-all.sh

./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```

设置SSTap进行加速测试是否正常

## 安装nodejs和npm
```bash
curl https://raw.githubusercontent.com/creationix/nvm/v0.13.1/install.sh | bash

source ~/.bash_profile

nvm install v9.8.0

nvm alias default v9.8.0
```
## 安装libpcap
```bash
yum -y install gcc-c++

yum -y install flex

yum -y install bison

wget http://www.tcpdump.org/release/libpcap-1.8.1.tar.gz

tar -zxvf libpcap-1.8.1.tar.gz

cd libpcap-1.8.1

./configure

make

make install
```

## 安装部署项目
```bash
yum install git

git clone git://github.com/yueyun2018/PUBG-Radar-Onekey

cd PUBG-Radar-Onekey/

npm i

npm i -g pino

npm install -g forever
 
forever start index.js sniff eth0 127.0.0.1 | pino

```

## Link

Local computer using SSTAP connection

Watching address  serverIP:20086/


Restart PUBG-Radar command

```bash
cd /root/PUBG-Radar-Onekey;. restart.sh
```
