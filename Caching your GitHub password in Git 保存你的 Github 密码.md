Caching your GitHub password in Git 保存你的 Github 密码
===========

如果是 [使用 HTTPS 来复制 github 项目库](https://help.github.com/articles/which-remote-url-should-i-use)， 可以使用 credential helper 来 告诉 Git 记住你的 Github username 和 password ，当你跟 github 交互时。

如果你使用的 是 SSH ,你通过 SSH keys 来代替 username 和 password 实现验证。有关设置，查看[Generating SSH Keys](https://help.github.com/articles/generating-ssh-keys)

*提示: 需要 Git 1.7.10 或更新的版本来支持 credential helper.*

如果你安装了 [Github 客户端](https://windows.github.com/)，credential helper 已经包含在内，这个应用也包含了一个 Git shell, 所以不需要和配置 Git 了。

如果你使用命令行，你可以安装一个原生的 Git shell, 比如 [msysgit](https://msysgit.github.io/),使用下列命令行来储存你的验证。

	git config --global credential.helper wincred

*参考*：[https://help.github.com/articles/caching-your-github-password-in-git/
](https://help.github.com/articles/caching-your-github-password-in-git/
)
