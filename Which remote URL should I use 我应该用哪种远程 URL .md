Which remote URL should I use 我应该用哪种远程 URL
===========

在 Github 中有几种方式来复制项目库。如下图

![URL](https://help.github.com/assets/images/help/repository/remotes-url.png)

如何设置，查看 [Changing a remote's URL.](https://help.github.com/articles/changing-a-remote-s-url)

##Cloning with HTTPS (recommended) 推荐使用 HTTPS

`https://` 克隆的网址上所有可用的库，公共和私人的。他们很智能，所以他们会为你提供只读或读/写访问，这取决于你的库的权限。

这些URL无处不在——即使你是在防火墙或代理。在某些情况下，如果你想使用SSH，你可以[使用SSH的端口](https://help.github.com/articles/using-ssh-over-the-https-port)。

当你git fetch, git pull, 或 git push 使用远程存储库时，需要 提供 GitHub 的 username 和 password 。 
* 如果你启动了 [双重认证](https://help.github.com/articles/about-two-factor-authentication),你必须 [创建个人访问 token](https://help.github.com/articles/creating-an-access-token-for-command-line-use)来代替你的 Github password
* 如果你使用 [credential helper](https://github.com/waylau/github-help/blob/master/Caching%20your%20GitHub%20password%20in%20Git%20%E4%BF%9D%E5%AD%98%E4%BD%A0%E7%9A%84%20Github%20%E5%AF%86%E7%A0%81.md),Git 将会记住你的 Github, username 和 password 当你跟 Github 交互时。

##Cloning with SSH 使用 SSH

这些链接提供通过 SSH 的 Git 仓库，这是一个安全协议。使用这些链接，你必须有一个 [SSH 密钥对](https://help.github.com/articles/generating-ssh-keys) 在您的计算机生成的，并连接到你的GitHub帐户。

GitHub 的桌面客户端自动配置SSH钥匙给你，如果你不想纠结在命令行。

*提示：SSH 网址可以在本地使用，或作为一个安全的方式部署到生产服务器代码。您还可以使用 SSH 代理转发您的部署脚本来避免管理服务器上的密钥。*

##Cloning with Subversion 使用 Subversion

同样，你可以使用 [Subversion](https://subversion.apache.org/) 客户端 来访问 Github。 Subversion 提供了比 Git 更多特性设置,详见 [SVN 和 Git 的不同点](https://help.github.com/articles/what-are-the-differences-between-svn-and-git)

一个单独的文章[更多的信息关于怎样使用 Subversion 与 GitHub 互动](https://help.github.com/articles/support-for-subversion-clients)。

##Further reading 延生阅读

* Pro Git 书中关于"[Working with Remotes](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes)"


*参考*：[https://help.github.com/articles/which-remote-url-should-i-use/
](https://help.github.com/articles/which-remote-url-should-i-use/
)
