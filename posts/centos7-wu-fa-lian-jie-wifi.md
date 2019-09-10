---
title: 'centos7无法链接wifi'
date: 2019-09-08 17:16:44
tags: []
published: true
hideInList: false
feature: 
---
centos7无法链接wifi

输入以下代码：
# rfkill unblock all
# rfkill list
# modprobe -r ideapad_laptop

这样就解决 NO WIFI adapter found.
