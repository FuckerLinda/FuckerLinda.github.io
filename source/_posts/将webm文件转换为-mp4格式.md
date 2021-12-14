---
title: 将webm文件转换为.mp4格式
toc: true
date: 2021-12-14 21:59:57
tags:
categories:
---

`brew install ffmpeg`

`ffmpeg -i input.webm -c:v libx264 -c:a aac -strict experimental -b:a 192k output.mp4`

（该参数对音频使用192 kBit / s恒定比特率）



对于音频，静态构建不支持`libfdk-aa`。如果你支持它，则应改用：`ffmpeg -i input.webm -c:v libx264 -c:a libfdk_aac output.mp4`

## 参考资料

> - [如何将Macm的webm转换为mp4](https://qastack.cn/superuser/523252/how-do-i-convert-webm-to-mp4-for-macosx)
