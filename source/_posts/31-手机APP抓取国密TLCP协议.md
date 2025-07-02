## 一、准备工具

1、v2ray：https://github.com/2dust/v2rayn/releases?after=latest

2、gost：https://github.com/go-gost/gost/releases/tag/v3.0.0

3、gmsocks：https://www.gmssl.cn/gmssl/index.jsp

4、wireshark：https://www.wireshark.org/download.html

5、PC

6、同个网络

## 二、配置v2ray

在设置中需要开启允许局域网连接

![image-20250602194310857.png][1]

添加一个sockes代理

![image-20250602194935047.png][2]

## 三、配置gost

这里gost的作用是把v2ray的socks代理的**5437端口**转发到gmsocks的**1080端口**，下载后解压，在目录的地址栏执行cmd后执行启动命令

![image-20250602195656628.png][3]

在命令行窗口执行命令：`gost.exe -L tcp://:5437/127.0.0.1:1080`

![image-20250602195755134.png][4]

之所以需要用到gost，是因为gmsocks软件只监听本地回环地址127.0.0.1:1080，而使用了gost可以设置监听所有地址0.0.0.0:5437,然后让gost接收到的TCP/UDP流量转发到gmsocks。

![image.png][5]

## 四、gmsocks配置

下载解压后执行命令：`gmsocks`

![image-20250602200017635.png][6]

## 五、手机配置

手机下载安装v2rayNG

https://github.com/2dust/v2rayNG/releases?after=0.6.11

![image-20250602200908718.png][7]

## 六、访问国密网站

以中国银行提供的国密网站进行测试：https://ebssec.boc.cn/boc15/login.html

开启代理访问：

![image-20250602201909771.png][8]

关闭代理访问：

![image-20250602202125505.png][9]

## 七、wireshark抓包

在PC端使用wireshark抓取TLCP协议报文

![image-20250602202610940.png][10]

拓扑图参考如下图所示：

![image.png][11]


[1]: https://2c67fdf.webp.li/5e88d5ddcacaf57b4fea476ba11381f6.png
[2]: https://2c67fdf.webp.li/bfc08e0c9b2502867a293469ea678e09.png
[3]: https://2c67fdf.webp.li/b959f47d86a9914b2ea81782a3b20ef4.png
[4]: https://2c67fdf.webp.li/91ef01ce6c340e36ba24e3c0784e6871.png
[5]: https://2c67fdf.webp.li/5cb9186a40253667de037de209d1a0ed.png
[6]: https://2c67fdf.webp.li/419dd1a450f7721b469d962446796b1a.png
[7]: https://2c67fdf.webp.li/6e64abfc2bda367856790cdb37503fa9.png
[8]: https://2c67fdf.webp.li/54f7e49be1a152ca04528cc316788881.png
[9]: https://2c67fdf.webp.li/f04fc14fe335d0dc2966ccf2b19846fa.png
[10]: https://2c67fdf.webp.li/1388d36b2f609b33ed987da60e31ae9b.png
[11]: https://2c67fdf.webp.li/79454958f9559c475bab84b464abca95.png

