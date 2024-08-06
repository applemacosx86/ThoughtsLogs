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

## 另外一篇相关文章
消除叹号，同步网络时间
https://www.dongyao.ren/article/316.html
WIFI 小叉叉消除只要输入下面 4 行命令即可

删除旧的监测点
```
adb shell settings delete global captive_portal_https_url
adb shell settings delete global captive_portal_http_url
```
添加新的监测点
```
adb shell settings put global captive_portal_https_url https://connect.rom.miui.com/generate_204
adb shell settings put global captive_portal_http_url http://connect.rom.miui.com/generate_204
```


时间同步问题  
因为时间同步的服务器也是在国外的，因此我们也需要将其修改为国内 NTP 服务器，我们只需要在 adb 中输入以下内容即可

设置中国时区
```
adb shell setprop persist.sys.timezone Asia/Shanghai
```
设置 NTP 服务器
```
adb shell settings put global ntp_server ntp1.aliyun.com
```

到这里就处理好了，打开飞行模式，然后重新关闭飞行模式，让手机自动进行重新连接，会发现这两个问题都正常了。