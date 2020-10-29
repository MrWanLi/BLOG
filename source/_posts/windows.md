---
title: windows启动命令
date: 2020-10-22 13:58:38
categories: [programme]
tags: [windows]
index_img: /img/logo/windows.jpg 
banner_img: /img/bg/asoggetti-44oFcp01cVU-unsplash.jpg
excerpt: windows(一)
---

### windows杀进程
  netstat -ano  查看所有端口使用情况
  netstat -ano |findstr "端口号"  查看指定端口使用情况
  taskkill |findstr "进程ID"      查看进程ID
  taskkill  /f  /t /im "进程ID"

### activemq启动 
  cmd 进入activemq安装路径
  activemq start 启动
  http://127.0.0.1:8161/ 查看是否启动



