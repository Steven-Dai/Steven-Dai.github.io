---
layout: blog
title: deepin配置Java开发
background-image: 
date:  2020-06-16 23:45:56
category: git
tags:
- deepin

---
Deepin系统配置JAVA开发环境，安装jdk、git、maven.

# 安装jdk8
```
搜索JAVA安装包
sudo apt-cache search jdk
安装
sudo apt-get install openjdk-8-jdk
验证
java -version
```

# 安装git
```
sudo apt-get update
sudo apt-get install git

保存密码，不用每次都输入密码
git config --global credential.helper store
```

# 安装maven
```
下载并上传maven安装包 http://maven.apache.org/download.cgi
解压并配置settings.xml
配置阿里云镜像
<!-- 阿里云仓库 -->
<mirror>
    <id>alimaven</id>
    <mirrorOf>central</mirrorOf>
    <name>aliyun maven</name>
    <url>http://maven.aliyun.com/nexus/content/repositories/central/</url>
</mirror>
<!-- 中央仓库1 -->
<mirror>
    <id>repo1</id>
    <mirrorOf>central</mirrorOf>
    <name>Human Readable Name for this Mirror.</name>
    <url>http://repo1.maven.org/maven2/</url>
</mirror>

sudo vi /etc/profile
sudo source /etc/profile

验证
mvn -v
```
