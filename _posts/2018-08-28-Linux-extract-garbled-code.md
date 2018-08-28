---
layout: post
title: Linux，Mac解压乱码的终极完美方法
categories: [教程]
description: Linux解压乱码的终极完美方法
keywords: Linux, 乱码， Mac， unzip， 解压密码
---
# Linux，Mac解压乱码的终极完美方法

## Linux Mac解压Windows的文件时 一般都会遇到文件名中文乱码的情况。
## 网上流传的一般方法时unzip -O命令，但是许多unzip版本并没有-O参数，而且如果文件带密码， 会出现解压失败的Bug。

# 下面就提供一种Linux Mac完美解压文件无乱码的方法

## 非常简单 安装 unar 工具 支持几乎所有格式

ubuntu 等debian系Linux采用

```shell

sudo apt install unar

```
redhat系Mac系自行查找安装unar命令

使用

```shell

unar filename

```
即可解压
自动判断编码格式

而且如果文件需要密码会提示输入，完美解决问题。