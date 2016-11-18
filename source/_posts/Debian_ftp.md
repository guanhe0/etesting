---
title: ftp
date: 2016-11-16 15:04
tags:
    - Debian
  categories:
  - Server
---

## On Debian
### 安装应用

```bash
apt-get install vsftpd -y 
```

### 启动ftp服务

```bash
service vsftpd start

```

### 停止ftp服务
```bash
service vsftpd stop
```

### 重启ftp服务
```bash
service vsftpd restart
```
### 获取到系统IP

```bash
ifconfig -a
```
在windows系统使用winscp或者类似ftp软件，进行如下设置：
1、文件协议：sftp
2、主机名：192.168.1.xxx
3、端口号：22
4、输入发行版系统的用户名和密码登陆即可(使用root/root)

