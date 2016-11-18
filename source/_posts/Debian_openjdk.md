---
title: openJDK
date: 2016-11-16 16:13
tags:
    - Debian
categories:
  - Server
---

## On Debian
### 安装应用

```bash
apt-get install openjdk-7-jre -y
apt-get install openjdk-7-jdk -y

```

### 添加JDK环境变量

```bash
export JAVA_HOME=/usr/lib/jvm/java-7-openjdk-i386
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
export PATH=${JAVA_HOME}/bin:${JRE_HOME}/bin:$PATH
```
### 重启系统检查JAVA配置

```bash
$env
$java -version
$echo $JAVA_HOME
```
如果以上命令都有输出信息代表成功
