---
layout:     keynote
title:      "在光猫/软路由上使用 Cloudflare 的动态域名"
subtitle:   "Using Cloudflare's Dynamic Domain Name"
iframe:     "/_includes/2024-01-20/yanshuo.html"
navcolor:   "invert"
date:       2024-01-20
author:     "ifeng"
tags:
    - Cloudflare
    - DDNS
---

> 下滑这里查看更多内容

　　相信很多小伙伴对于动态域名已经很熟悉了，大多数光猫/路由器也都内置了 DDNS 功能。但是在使用过程中，好像总是有点掣肘，例如一些早期的光猫/路由器提供的 DDNS 功能只支持更新 IPv4 地址，由于移动宽带只提供公网的 IPv6 公网地址，DDNS 功能会无法使用。因此在两年前，我就写了两段简单的 DDNS 更新脚本，使用 DnsPod.cn 或 dynv6.com 动态域名完成 IPv4&IPv6 地址的更新。

　　现在看来，使用 DnsPod.cn 或 dynv6.com 动态域名仍然有一些不完美的地方，由于三大运营商都关闭了家庭宽带的 80 & 443 端口，如果想利用家庭宽带搭建一个 Blog ，或者将自己群晖里的内容分享给其他朋友使用时，总要在网址后面带上端口才可以访问。如果使用 Cloudflare.com 的动态域名，另外配合 Cloudflare Origin Rules 功能，即可完美解决上述问题。
