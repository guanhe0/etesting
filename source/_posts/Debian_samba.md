---
title:  Samba
date:   2016-11-16 13:55
tags:
  -  Debian
categories:
  -  Server
---

## On Debian

### 更新源
```bash
apt-get update -y
```


### 安装应用

```bash
apt-get install samba -y
```

### 添加linux用户,并设置linux用户smb密码

```bash
adduser  smb
```



### 设置samba用户smb的密码

```bash
smbpasswd -a smb
```
###  修改配置文件/etc/samba/smb.conf
添加如下配置项

```
[share]
 comment = Root Directories
 writeable = yes
 security = share
 path= /opt/share
 browseable = yes
 public = yes
```

### 重启samba服务器

```bash
/etc/init.d/smbd restart 
如果上面的命令失败就用：systemctl restart nmb.service smb.service
```

### 查看samba服务器IP地址

```bash
ifconfig -a
```

在windows系统cmd输入:`\\192.168.1.xxx`
如果可以打开并看到share文件代表samba成功

