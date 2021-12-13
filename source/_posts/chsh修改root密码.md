---
title: chsh修改root密码
toc: true
date: 2021-12-13 09:55:35
tags:
categories:
---

root用户下使用chsh，若错误修改shell路径（比如改为haha），root用户的shell仍会被强制修改（如 改为haha）。

这样，之后便不能再切换至root用户。



解决方案：

`cd /etc/passwd`

找到root用户一行（如`　root:x:0:0:root:/root:haha`）

修改其shell（将`haha`改为原来的shell，如`/usr/bin/bash`）


