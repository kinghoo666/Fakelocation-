# Fakelocation

简介
一个FakeLocation应用程序的模拟验证服务器

解锁了app的所有pro功能，去掉了限制使用的app和限制使用的功能

如何使用
我只测试了1.3.0.2的版本，所以我建议你使用和我一样的版本，因为新版本中加入了https，不太方便模拟服务，功能差不了多少

你可以从这里下载，或者从release下载：

下载链接1

先克隆项目：

git clone https://github.com/BobH233/FakeLocation-server.git
在服务器上安装nodejs

运输安装依赖

npm install
运行下命令启动服务器，确保8000端口不被占用

node index.js
接下来你需要把手机的所有有关验证服务的域名称重定到你自己的服务器ip上，下面提供两种方法

重定向完成后，打开app并随即输入一个邮箱密码登陆即可永久使用

设置代理重定向
下面两种方法，随意选择一种即可

1.路由器法 (OpenWRT系统)
去网络 > DNS/DHCP > 自定义域名劫持

然后把下面三个域名称劫持到你自己的服务器ip上

fakelocation.api.lerist.cc -> your server ip
notice.api.lerist.cc -> your server ip
ads.api.lerist.cc -> your server ip
2.虚拟主机软件
你可以在这里下载Virtual Hosts: Release 2.1.0 · x-falcon/Virtual-Hosts (github.com)

假设你的服务器ip是192.168.1.5，那么你就编写如下的hosts.txt，然后用Virtual Hosts选择这个hosts文件

192.168.1.5 fakelocation.api.lerist.cc
192.168.1.5 notice.api.lerist.cc
192.168.1.5 ads.api.lerist.cc
设置完成后，使用手机浏览器访问fakelocation.api.lerist.cc:8000/

如果能够正确访问并显示版本号，证明成功配置

为什么我要做这个服务器
首先，特别感谢原作者编写的这十分钟有用的app，给我提供了方便

你应该钱也赚够了，现在我们都喜欢“开源”

我觉得你把这种本应该方便大家的软件设置硬性价格不太合理，为什么不把软件开源，以赞帮助的形式来恰饭呢？
