title: web remote connect
date: 2020-08-16 10:32:06
---
## 搭建一个web远程连接的服务

1、基于ssh协议的linux机器连接
**架构：** angular + springboot + tornado
**实现原理：** 前端与python端建立websocket连接用于实时返回命令执行的结果，springboot端用于执行和审计命令等操作进行功能增强
**实现步骤：**

1. 先打通连接，实现最主要的功能（前端画布展示并且能够输入命令执行，python实现ssh2协议连接到目标主机且使用tornado web框架建立websocket接口，打通前端到python端）
2. todo: 后续功能增强

2、基于rdp协议的windows机器连接
**架构：** angular + springboot + guacamole-server
**实现原理：** 互相之间建立websocket连接，实时传送数据，springboot可以添加很多增强的功能比如录屏和获取延时