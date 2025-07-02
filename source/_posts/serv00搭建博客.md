---
title: serv00服务器
date: 2025-01-10 09:51:27
tags: 技术
---

# 一、serv00服务器

## 1.1 SSH登录serv00服务器

主机（H）的`s6.serv00.com`可能用不了，可以使用`web6.serv00.com、cache6.serv00.com、pane6.serv00.com、panel6.serv00.net、liyilin.serv00.net`替换。

![xshell登录serv00](https://2c67fdf.webp.li/418c448a4d084cb3c60f28ed60236590.png)

## 1.2 进入博客主路径

```shell
cd domains/liyilin.serv00.net/public_html
```

## 1.3 下载博客软件

下载typecho程序到目录

```shell
wget https://github.com/typecho/typecho/releases/latest/download/typecho.zip
```

## 1.4 解压文件

```shell
unzip typecho.zip
```

# 二、登录博客

![typecho首页](https://2c67fdf.webp.li/3548d7f3f95727bd6af8265a25fcd420.png)

安装过程中唯一难度就是这个**数据库信息**，首先**网页登录**serv00，创建数据库。

![image-20250109104417180](https://2c67fdf.webp.li/34806cf10538b202933f2a37cadf1f58.png)

然后把数据库信息填入 typecho 安装界面

![serv00配置信息填入typecho安装界面](https://2c67fdf.webp.li/5c4aaa160cf805a1efb673b39a8f44fa.png)

WEB界面：https://panel6.serv00.com

博客管理员控制台：https://liyilin.serv00.net



