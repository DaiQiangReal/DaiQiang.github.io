---
layout: post
title: Linux 系统批量安装字体的方法
categories: [教程]
description: Linux 系统批量安装字体的方法
keywords: Linux,字体
---
# Linux 系统批量安装字体的方法

## 下载字体
1. 下载需要安装的字体（ttf格式），或者直接从其他windows系统c:\windows\Fonts 下复制。
## 安装字体
2. 将所有的ttf格式的字体文件复制到/usr/share/fonts/custom 文件夹下（custom 文件夹自己创建）
3. 打开终端 输入 
```shell
sudo fc-cache -fv
```
刷新字体缓存。
## 字体批量安装成功