Why are my contributions not showing up on my profile 为毛Github的contributions贡献值不增长了
===========

近期发现每天在 Github 做代码提交，但是 contributions 的面板（贡献图）上的绿点（即贡献值）却没有增长了。擦~ 有两个礼拜了。如下图

![contributions](http://i1288.photobucket.com/albums/b484/waylau/waylau%20blog/003_zps420c5beb.jpg)

而且，同时发现以前的绿点也是稀稀拉拉的，遂感觉 contributions 可能被漏记了。看了下 Github 对于  contributions 的 [说明](https://help.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profile/)更新时间是在昨天（2014-10-17），说明 contributions 的统计策略是经常改变的。

本文详细说明了如何contributions贡献值是如何统计的。同时参照最新的 contributions 的 [说明](https://help.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profile/)（时间 2014-10-17），并且在以后会同步官网的更新，方便各位网友。

#哪些 contributions 贡献值会被统计

##Issues and pull requests 问题和请求

问题和请求将出现在您的贡献图上需满足下面这两个条件：

* 他们开启的时间是在过去的一年。
* 他们开启的时候是一个独立的存储库，不是 fork 来的库

##Commits 提交

提交将出现在您的贡献图上，如果它们满足*所有*以下条件：

* 在过去的一年之内作出的提交。
* 用于提交的电子邮件地址是与您 GitHub 帐户相关联。
* 提交是在一个独立的库，不是 fork 来的库
* 提交是在库的默认分支。

此外，*至少其中一项*必须为真：

* 你是存中的合作者或拥有库的组织中的成员。
* 你 fork 了库。
* 你已经在存中打开一个拉请求或问题。
* 你给库打了星星。
 
*私人库的贡献只会显示给可以访问这些库的用户。这些贡献都不会呈现给无法访问这些库的用户。*

#贡献不被计算在内的常见原因

##你还没在你 GitHub 配置文件中添加你本地 Git 提交的电子邮件

提交时必须采用已添加到您 GitHub 的配置文件，出现在你的贡献图上的电子邮件地址。您可以检查电子邮件通过将.patch 添加到用于提交 URL 后面，例如 https://github.com/octocat/octocat.github.io/commit/67c0afc1da354d8571f51b6f0af8f2794117fd10.patch ：

>From 67c0afc1da354d8571f51b6f0af8f2794117fd10 Mon Sep 17 00:00:00 2001
From: The Octocat
Date: Sun, 27 Apr 2014 15:36:39 +0530
Subject: [PATCH] updated index for better welcome message

其中电子邮件的格式： 字段是在本地 git 的[配置](https://help.github.com/articles/set-up-git)设置中设置的地址。在此示例中，用于提交的电子邮件地址是 octocat@nowhere.com。

如果没有被用于提交的[电子邮件地址添加](https://help.github.com/articles/adding-an-email-address-to-your-github-account)到您 GitHub 的配置文件，您必须将电子邮件地址添加到您的 GitHub.com 帐户或 GitHub 企业帐户。当您添加新的地址时，您的贡献图将自动重建。

*一般的电子邮件地址——如 jane@computer.local——不能添加到 GitHub 帐户。如果您使用此类电子邮件为您的提交，提交将不被链接到 GitHub 配置文件并不会显示在您的贡献图。*

##提交了一个非默认分支

提交只能是在默认分支 （通常`master`）被统计。如果你想在非默认分支中，希望他们能计入您的贡献，需要执行以下任一操作：

* 打开一个要更改合并到默认分支中的 [pull 请求](https://help.github.com/articles/creating-a-pull-request)。
* 更改库中的[默认分支](https://help.github.com/articles/setting-the-default-branch)。

*更改存库中的默认分支将更改它的所有库中的合作者。只能这样做，如果你想要新分支成为所有未来的请求和提交所针对的基础。*

##在 fork 中做了提交

在一个 fork 作出的提交将不计入你的贡献。要使它们计数，必须执行下列操作之一：

* 打开一个要更改合并到父资源库中的 [pull 请求](https://help.github.com/articles/creating-a-pull-request)。
* 脱离 fork 并将在 GitHub.com 或 GitHub Enterprise中独立的库，分别联系 GitHub 的[客服](https://github.com/contact)或您的站点管理员。


*参考*：[https://help.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profile/
](https://help.github.com/articles/why-are-my-contributions-not-showing-up-on-my-profile/
)
