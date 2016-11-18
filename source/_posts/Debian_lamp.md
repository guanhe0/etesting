---
title: lamp
date: 2016-11-16 15:49
tags:
    - Debian
categories:
  - Server
---

## On Debian
### 安装应用apache2

```bash
apt-get install apache2 -y 
```
### 获取到系统IP

```bash
ifconfig -a
```
在其它PC机上以http://192.168.1.xxx的方式访问apache服务器，能打开apache欢迎页面说明apache服务器安装成功

### 安装应用php5
```bash
apt-get install php5 -y
```
###在终端执行命令
```bash
echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/testing.php 
```
### 获取到系统IP

```bash
ifconfig -a
```
在其它PC机上以http://192.168.1.xxx/testing.php的方式访问php服务，能打开php信息显示页面说明php安装成功

