---
layout: default
title: 微信公共平台之订阅号
---

今天申请了微信公共平台的开发资格，架设了一个基本的订阅号：mysql。支持文本交互，可发送1,2,3,4,5，6,7得到预定好的回复。

采用了Google APP Engine作为网络服务器，用python实现。计划以后可以支持人工智能自动答复。就好比苹果的siri机器人。

在微信平台的开发过程中，碰到了几个问题，费了很大的力气才解决。这正应了那句话：难了不会，会了不难。

问题1：HTTP 405 Method Not Allowed
  是由于我把post方法打错成了put方法，这两个目的是不一样的。惭愧惭愧！
  
问题2：unicode编码问题
  由于中文在python世界中需要变成unicode编码，才能在不同语言范围内流通，也就是要str.decode('utf-8')
  
问题3：防火墙的问题
  祖国把外国的新技术都封锁掉了，造成国内几乎都不能用，这也引起百度，QQ等公司的一家独大。这真是应了“山中无老虎，猴子称大王”。
  解决办法：有人搭设了一个代理appsp0t.com，可以绕道访问appspot.com，但是这个代理服务器有没有木马就不知道了，不怕死的就大胆用吧。