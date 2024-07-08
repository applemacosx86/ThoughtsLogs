---
title : 'Surge Memo'
date : 2024-07-09T01:20:09+08:00
draft : false
<!--cover: 
    image: imgs/papermod-cover.png
    alt: This is the cover image
    caption: screenshot-->
tags: [surge]
categories: [tech,memo,proxy,network]
---
## 增强模式下(Enhanced Mode) skip-proxy 无效
[官网论坛解释](https://community.nssurge.com/d/526-skip-proxy)
增强模式是虚拟网卡接管，skip-proxy 是跳过系统代理接管

[官方文档](https://manual.nssurge.com/others/misc-options.html)

> Notice: If you enter an IP address or address range, you are only able to bypass the proxy when you connect to that host using that address, not when you connect to the host by a domain name that resolves to that address.

直接访问 192.168.50.0/24 范围内的地址可以被跳过，但如果是访问的域名解析到这个范围内就没法跳过了