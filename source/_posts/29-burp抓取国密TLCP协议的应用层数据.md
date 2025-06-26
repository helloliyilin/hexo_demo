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


[1]: https://blog.lyl.us.kg/usr/uploads/2025/05/62282362.png
[2]: https://blog.lyl.us.kg/usr/uploads/2025/05/2352069310.png
[3]: https://blog.lyl.us.kg/usr/uploads/2025/05/1798545061.png
[4]: https://blog.lyl.us.kg/usr/uploads/2025/05/1138469997.png
[5]: https://blog.lyl.us.kg/usr/uploads/2025/05/576173719.png
[6]: https://blog.lyl.us.kg/usr/uploads/2025/05/3307012428.png
[7]: https://blog.lyl.us.kg/usr/uploads/2025/05/4257471371.png
[8]: https://blog.lyl.us.kg/usr/uploads/2025/05/1068805164.png
[9]: https://blog.lyl.us.kg/usr/uploads/2025/05/692629666.png
[10]: https://blog.lyl.us.kg/usr/uploads/2025/05/1756467834.png
[11]: https://blog.lyl.us.kg/usr/uploads/2025/05/2781441250.png
