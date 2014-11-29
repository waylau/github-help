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
* 所有的 Git 信息包括提交，包含提交，合作者会保存，除非 Git 历史被 `[git rebase]()` 从写。

*参考*：[https://help.github.com/articles/transferring-a-repository/](https://help.github.com/articles/transferring-a-repository/)
