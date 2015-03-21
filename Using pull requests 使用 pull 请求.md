Using pull requests 使用 pull 请求
===========

pull 请求让你告诉别人你 push 了一个更改到存储库。一旦 pull 请求被发送，关注的组织可以查看设置的变化，讨论可能的修改，甚至  push 后续的提交如果有必要。

本文演示了一个完整的过程。

##Types of collaborative development models 协同开发模式类型

主要是两种： Fork & pull 和 共享存储库.

###Fork & pull 

Fork & pull 可以让任何人 fork 现有的存储库，提交更改到他们个人的 fork 而无需访问授权到源存储库。这些变化必须再 pull 进该项目维护者的源存储库。这种模式减少的新贡献者的摩擦，在开源项目中比较流行，因为它使人们能够独立工作，无需前期的协调。

###共享存储库

他享仓库模型是小团队和组织合作开展私人项目更为普遍。每个人都被授予推访问一个单一的共享资源库和专题分支用于隔离的变化。

pull 请求是在 fork＆pull 模型中特别有用，因为它们提供了一种方法来通知项目维护者的变化中的 fork 。但是，他们同样适用于共享存储库模式，在他们用来启动代码审查和一般性讨论有关一组变化被合并到主线分支前。

##Before you begin 开始之前

首先你要有 [Github 账号](https://github.com/signup)，了解如何 fork 和 push ，见 [Fork A Repo](Fork A Repo.md) 

*参考*：<https://help.github.com/articles/using-pull-requests/>