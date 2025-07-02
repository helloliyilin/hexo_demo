---
title: burp抓取国密TLCP协议的应用层数据
date: 2025-06-10 10:46:29
tags: 工具
---

## 1、安装gmsocks代理
https://www.gmssl.cn/gmssl/index.jsp
![image.png][1]

## 2、启动gmsocks
在指定的目录下执行cmd命令
![image.png][2]
```bash
.\gmsocks -a 0.0.0.0 -p 1080
```
![image.png][3]
## 3、burp配置
❶添加本地http代理，127.0.0.1:8080
![image.png][4]
❷浏览器安装代理插件，使数据交给本地burp代理
![image.png][5]
❸burp设置上游gmsocks代理
![image.png][6]
❹网络拓扑参考如下
![image.png][7]
❺此时访问国密网站就抓到应用层数据包
国密测试网站：https://ebssec.boc.cn
没有开启代理访问网站的情况
![image.png][8]
开启代理访问网站的情况
![image.png][9]

## 4、抓包
使用wireshark抓包
![image.png][10]
查看burp抓包取应用层数据
![image.png][11]


[1]: https://2c67fdf.webp.li/a5643463482880ade06b8350c55ec710.png
[2]: https://2c67fdf.webp.li/e30d12fa63b7485e70131be82e4e953a.png
[3]: https://2c67fdf.webp.li/9342e8b574af4d2c7db982f7396cdf0d.png
[4]: https://2c67fdf.webp.li/931e83ed5db07b0c699e1e8dda8c3e11.png
[5]: https://2c67fdf.webp.li/ca1050a8f3b4380d0df81fbf5626834d.png
[6]: https://2c67fdf.webp.li/263d3f97b041121503dcbca517c53b9f.png
[7]: https://2c67fdf.webp.li/b61f66ecd9dcf63f949f9ed46a478fdd.png
[8]: https://2c67fdf.webp.li/64447ae86583ab8ac391278b9f1cc5bd.png
[9]: https://2c67fdf.webp.li/9fa67d0031ef2a810b1a23582bae6f37.png
[10]: https://2c67fdf.webp.li/c107234ceb584222fb6b1e8ab6e81b79.png
[11]: https://2c67fdf.webp.li/b182a82498f2c69b7e1fc592c237d973.png

