---
layout: post
title: 安卓系统启动终端不限速下载百度网盘
categories: [教程]
description: 安卓系统启动终端不限速下载百度网盘
keywords: 百度网盘, 不限速，BaiduPCS-Go，baidupcs
---
# 安卓系统启动终端不限速下载百度网盘

百度网盘是个好东西，网络上有许多资源都以百度网盘的形式分享。但百度网盘因为特殊原因，对非会员用户限制速度，在非p2p资源的情况下，下载速度往往在100KB/s以下，p2p下载也会被限速。下面将介绍在非root通用Android系统上使用百度pcs接口，不限速下载。方法windows, Linux，Mac os, Freebsd, Android, ios,主流全平台通用。
        
`程序开源代码在文末分享，BaiduPCS-Go版权为iikira所有，感谢其对开源社区的无私奉献。`

## 1.启动环境配置 
Android系统本质上是建立在Linux内核的一个特殊Linux发行版。本质上和Ubuntu等广为人知的Linux发行版并无区别，但是经过Google的修改，Android系统上并没有通常存在于Linux发行版上的终端模拟器。但是我们的教程所使用的程序代码是建立在命令行交互界面（CLI）上的，为了使用程序，我们必须在Android系统上安装终端模拟器。
	建议使用NeoTerm 即可，下载安装。

## 2.下载程序，并移动到指定位置	
下载对应平台的BaiduPCS-GO
	
如果我们通过 ./baidupcs(如果你的BaiduPCS-GO可执行程序文件名是这个)，通常会出现Permissi Denied，如果我们尝试chmod +x baidupcs 也会提示权限不足。这是因为未获取root权限的安卓系统对每个程序的权限进行了严格的限制，这其中也包括我们的终端模拟器，我们不能随便修改以及执行文件。
为了运行baidupcs，我们有两条路可以走，一是赋予程序可执行权限，显然未root的安卓机无法做到这一点，二是可以将baidupcs移动到我们的终端模拟器具有完全权限的目录。
	
1.终端输入 
```pwd```
查看终端所在目录（建议使用NeoTerm终端，否则无法正确找到终端模拟器所在安装目录，无法继续操作）
这个目录就是终端默认目录，终端模拟器对此目录具有完全执行权限。
![enter image description here](https://s1.ax1x.com/2018/07/15/PMqjbV.jpg)
2. 复制baidupcs到这个目录
```cp /sdcard/baidupcs /data/data/io.neoterm/files/home```
(源目录为安卓内部存储目录，因为我是事先将BaiduPCS-Go重命名为baidupcs并移动到了内部存储，方便操作。复制到的目录为刚才pwd命令显示的目录,自己根据输出替换)
![enter image description here](https://s1.ax1x.com/2018/07/15/PMqxET.jpg)
##3. 赋予执行权限
```chmod 777 baidupcs```
![enter image description here](https://s1.ax1x.com/2018/07/15/PMqzUU.jpg)
赋予baidupcs可执行权限。
##4.执行程序
```./baidupcs```
![enter image description here](https://s1.ax1x.com/2018/07/15/PMLS5F.jpg)

<br>
<br>
<br>
## 在其他平台教程通用，适当变通即可
[BaiduPCS-Go下载地址](https://github.com/iikira/BaiduPCS-Go)

`BaiduPCS-Go版权所有为程序原作者iikira。本教程仅为在非root安卓上的使用指导`
	
​	

