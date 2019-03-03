---
layout: post
title: Linux 使用wget下载FTP服务器文件
categories: [教程]
description: Linux 使用wget下载FTP服务器文件
keywords: linux，下载, wget, 文件, ftp
---
# Linux 使用wget下载FTP服务器文件
```shell
wget -nH -m --ftp-user=你的用户名 --ftp-password=密码 ftp://你的ftp地址或ip:端口默认21/*
```

-nH：不创建以主机名命名的目录。
–cut-dirs：希望去掉原来的目录层数，从根目录开始计算。如果想完全保留FTP原有的目录结构，则不要加该参数。
-m：下载所有子目录并且保留目录结构。
–ftp-user：FTP用户名
–ftp-password：FTP密码
