Transferring a repository 转换库
===========
 
任何库都可以在用户或者组织之间转换。转换库，可以让新用户第一时间获取到库的管理级别的访问权限包括：代码，问题，pull 请求 和发布包。库的新拥有者一天内会收到一个 email进行确认 是接受还是拒绝。如果不接受，则转换不能完成。

*警告： Fork 和 转换库不是一个概念。Fork 只是 复制库*

##What's transferred with a repository? 转换了什么

当转换了库，它的 issues, wiki, star, 和 watcher 都一起转了。包括：

* 如果该库是 fork ,它仍然保留与上游库的关系
* 如果包含 GitHub Pages 站点，网络上库的连接和通过 Git 的活动点被重定向。然而，我们不把 GitHub库 相关的网页重定向。
* 如果库包含了 webhooks，服务，或部署的密匙，他们仍将在转换完成后保留。
* 如果库有 fork ，那么这些 fork 会关联新的 库。fork 你库的人将更新 远程 URL 到新的 Git 库，来继续 [开启 pull  请求](https://github.com/waylau/github-help/blob/master/Creating%20a%20pull%20request%20%E5%88%9B%E5%BB%BA%20pull%20%E8%AF%B7%E6%B1%82.md)。
* 所有的 Git 信息包括提交，包含提交，合作者会保存，除非 Git 历史被 `[git rebase](https://github.com/waylau/github-help/blob/master/About%20Git%20rebase%20%E5%85%B3%E4%BA%8E%20Git%20rebase.md)` 从写。

##How are issue assignees handled? 如何处理问题受让人

如果你将库从用户帐户转为组织，关联了组织成员的问题保持不变。所有其他人的问题将清除。只有组织拥有者可以创建新问题。

如果你将库从组织转为用户帐户，与库拥有者关联的问题将保留，其余删除。

当一个库是两个用户帐户之间转移，问题分配是完好的。

##Transferring between user accounts 两个用户帐户之间转移

转移前牢记：

* 目标帐户在同一网络中不能具有相同名称的库或者 fork
* 如果库是私人的，目标帐户必须具有至少一个未使用的私有库具有帐户支付。
* 私人 fork 不能转让。

###将库转给其他用户账户:

1.打开库的页面

2.点击 Settings 

![](https://help.github.com/assets/images/help/repository/repo-actions-settings.png)

3.点击 Transfer

![](https://help.github.com/assets/images/help/repository/repo-transfer.png)

4.确认

5.输入新拥有者的名称，点击  I understand, transfer this repo

![](https://help.github.com/assets/images/help/repository/repo-transfer-complete.png)

##Transferring between organizations 组织间转换

组织间转换，用户必须是组织的管理者或者是组织的拥有者。接收的组织也是一样。当库转换后，拥有者的组是唯一可以对库进行  read/write  访问，但他们可以选择添加其他组授予更多的 访问权限。详见[组织的权限级别](https://github.com/waylau/github-help/blob/master/Permission%20levels%20for%20an%20organization%20repository%20%E7%BB%84%E7%BB%87%E5%BA%93%E7%9A%84%E6%9D%83%E9%99%90%E7%BA%A7%E5%88%AB.md)

##Transferring from an organization to a user 组织转用户

进行转换，用户必须是组织的管理者或者是组织的拥有者。如果用户没有访问，一个临时的管理组可以仅在它下面创建用户和库。接收存储库的用户是唯一一个能执行转移。

##Transferring from a user to an organization 用户转组织

在接收前，用户必须具有管理或者是拥有的权限。如果用户不具备这样的权限，一个临时的管理组可以被他创建。发送库的用户是唯一一个能执行转移。

当库转换后，拥有者的组是唯一可以对库进行  read/write  访问，但他们可以选择添加其他组授予更多的 访问权限。详见[组织的权限级别](https://github.com/waylau/github-help/blob/master/Permission%20levels%20for%20an%20organization%20repository%20%E7%BB%84%E7%BB%87%E5%BA%93%E7%9A%84%E6%9D%83%E9%99%90%E7%BA%A7%E5%88%AB.md)

##Redirects and Git remotes 重定向以及 Git 远程

当库被转换，所有链接库自动从以前的位置重定向到新的位置。

除了重定向网站的流量，所有的 `git clone`，`git fetch`，或 `git push` 操作针对以前的位置将继续充当在新的位置。然而，这可有点混乱，所以我们强烈推荐更新任何现有的本地克隆以指向新库 URL。你可以用 git远程命令：

	$git remote set-url origin new_url

更多信息，见“[改变一个远程的URL](https://github.com/waylau/github-help/blob/master/Changing%20a%20remote's%20URL%20%E4%BF%AE%E6%94%B9%E8%BF%9C%E7%A8%8B%20URL.md)”。

*警告：如果你创建一个新的库在您的帐户具有相同名字的库，现有的重定向到转过来的库将打破。这样的话，为新的库使用不同的名称。*



*参考*：[https://help.github.com/articles/transferring-a-repository/](https://help.github.com/articles/transferring-a-repository/)
