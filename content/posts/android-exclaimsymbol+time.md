---
title : 'Android Exclaimsymbol+time'
date : 2024-08-06T20:51:34+08:00
draft : false
<!--cover: 
    image: imgs/papermod-cover.png
    alt: This is the cover image
    caption: screenshot-->
tags: [android]
categories: [tech,memo]
---

## 安卓去除叉x号或者感叹号的消除办法

(以下办法支持安卓11+)
adb shell settings put global captive_portal_mode 0
adb shell settings put global captive_portal_https_url https://www.google.cn/generate_204

(以下办法支持安卓10.0/9.0)
adb shell settings put global captive_portal_https_url https://www.google.cn/generate_204

然后开启飞行模式，然后关闭飞行模式解决！亲自测试有效！