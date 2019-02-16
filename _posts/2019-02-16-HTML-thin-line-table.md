---
layout: post
title: HTML 创建1像素细线表格方法
categories: [教程]
description: HTML 创建1像素细线表格方法
keywords: html, 像素， 细线， 细线表格， 教程
---
# HTML 创建1像素细线表格方法
html table绘制表格 即使table标签 设置 border="1" 仍然很粗 这是因为内外边框重合导致边框为2px
## 解决方法
 <xmp><table border="1" style="border-collapse:collapse;"></xmp>
 添加即可
 