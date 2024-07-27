---
title: Termux安装Linux系统及其桌面
layout: post
categories: [linux]
---

也是在安卓设备上用上Linux了


主要参考这些

> [Termux安装Linux系统及其桌面安装详细教程(附更改默认语言)](https://blog.csdn.net/zzhds/article/details/115976332)
> [Android Termux 安装 Linux 就是这么简单](https://www.sqlsec.com/2020/04/termuxlinux.html)

### Termux
Termux是一个适用于 Android 的终端模拟器，其环境类似于 Linux 环境。 无需Root或设置即可使用。 Termux 会自动进行最小安装 - 使用 APT 包管理器即可获得其他软件包。
### AnLinux(F-Droid)
https://f-droid.org/zh_Hans/packages/exa.lnx.a/ 
在没有root访问权限的情况下在Android上运行Linux 
### VNC Server
支持GUI
### 常用安装
```
apt update
apt upgrade
apt install -y git proot vim python
```
### 向导安装
```
git clone https://github.com/sqlsec/termux-install-linux
cd termux-install-linux
python termux-linux-install.py 

cd ~/Termux-Linux/Ubuntu
./start-ubuntu.sh
```
然后去AnLinux装系统，然后`./start-系统名字.sh`打开 
### 改中文
```
vim start-ubuntu.sh
```
`LANG=C.UTF-8`改为`LANG=zh_CN.UTF-8`
安装中文包
```
apt update
apt upgrade
apt install -y language-pack-zh-hans fonts-wqy-microhei
```
### END
启动
```
vncserver-start
```
关闭
```
vncserver-stop
```
在VNC Server新建连接 地址`localhost:1`






