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




*参考*：[https://help.github.com/articles/transferring-a-repository/](https://help.github.com/articles/transferring-a-repository/)
