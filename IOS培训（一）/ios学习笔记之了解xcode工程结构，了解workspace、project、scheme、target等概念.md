##IOS学习笔记之了解Xcode工程结构，了解Workspace、Project、Scheme、Target等概念
####From JiaYing.Cheng

---
---

###Xcode的一些结构概念

#####Workspace：
简单来说，Workspace就是一个容器，在该容器中可以存放多个你创建的Xcode Project， 以及其他的项目中需要使用到的文件。

使用Workspace的好处有：
1),扩展项目的可视域，即可以在多个项目之间跳转，重构，一个项目可以使用另一个项目的输 出。Workspace会负责各个Project之间提供各种相互依赖的关系;
2),多个项目之间共享Build目录。

#####Project：
指一个项目，该项目会负责管理生成一个或者多个软件产品的全部文件和配置，一个Project可以包含多个Target。

#####Target：
一个Target是指在一个Project中构建的一个产品，它包含了构建该产品的所有文件，以及如何构建该产品的配置。

#####Scheme：
一个定义好构建过程的Target成为一个Scheme。可在Scheme中定义的Target的构建过程有：Build/Run/Test/Profile/Analyze/Archive

#####BuildSetting：
配置产品的Build设置，比方说，使用哪个Architectures？使用哪个版本的SDK？。在Xcode Project中，有Project级别的Build Setting，也有Target级别的Build Setting。Build一个产品时一定是针对某个Target的，因此，XCode中总是优先选择Target的Build Setting，如果Target没有配置，则会使用Project的Build Setting。



1. [XCode 同一Project创建多个target](http://blog.163.com/lengfeng_04/blog/static/80470603201273111549529/)

2. [[译]iOS:Xcode一些概念Target|Project|Build Setting|Workspace|Scheme[译]Xcode Concepts](http://blog.csdn.net/houseq/article/details/24260917)

3. [workspace & subProject & target ](http://blog.itpub.net/12231606/viewspace-1079867)




