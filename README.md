# Wireboy.Socket.P2PSocket

喜欢此项目的，请点击一下右上角的Star

加入QQ群417159195，与作者共同交流，入群途径请填写“P2PSocket”

## 开发计划（开发顺序不分先后）

（已完成）~~1.客户端与服务端均增加日志功能~~

（已完成）~~2.客户端（主控端）增加断线重连功能~~

（已完成）~~3.为客户端与服务端增加配置文件~~

4.TCP点对点连接（不经过服务器）

5.客户端（被控端）增加密码验证

6.服务端增加用户名与密码验证（数据库）

## 当前项目状态？

1.master分支版本已稳定，但需要修改服务端ip编译后使用。

2.dev分支版本为开发者活跃版本，新功能会先加入dev分支，稳定后与master分支合并。

## 版本下载
	客户端下载 ：[点击下载](download/latest/P2PSocketClient.zip)
	服务端端下载 ：[点击下载](download/latest/P2PSocketServer.zip)

## 网络结构

![img4](Images/img4.png)

## 先来个项目介绍吧

此项目在正确设置服务端ip后，可用于mstsc进行远程桌面控制（我的目的也如此）。

这是一个使用.NetCore控制台项目作为服务端，.netframework4.5的C#控制台项目作为主控与被控客户端的项目。

结论：这是一个假的p2p服务

## 如何使用？

编译环境：VS2017 + .Net Framework 4.5  + .Net Core 2.1

1.修改P2PSocketClient的配置文件，将服务器ip与端口改为自己的公网ip服务器。

![img1](Images/img1.png)

2.在公网ip服务器部署并启动P2PSocketServer。（手动启动：在控制台输入 dotnet P2PSocketServer.dll）

3.将P2PSocketClient在被控制电脑启动，输入本地Home服务名称：home

4.将P2PSocketClient在主控电脑启动，输入远程Home服务名称：home

5.在主控电脑，启动mstsc，输入127.0.0.1:3388 进行远程连接

注：被控端电脑需要开启远程服务，如下图：

![img2](Images/img2.png)

## 运行效果图

![img3](Images/img3.gif)

## 更新日志

### 2019年3月15日

1.原Home服务端与原Client服务端合并

2.客户端完善断线重连功能，主控、被控与服务器可乱序启动

3.增加配置文件的读写

4.增加日志的读写

5.修复使用mstsc连接失败的问题

### 2019年2月20日

1.解决第二次连接失败的问题

2.增加被控端（Home）的日志记录功能




