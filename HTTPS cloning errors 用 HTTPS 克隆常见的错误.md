HTTPS cloning errors 用 HTTPS 克隆常见的错误
===========

几个常见的错误关于使用 HTTPS 和 Git。一般出错的原因是你的 Git 版本太旧或者没有访问库的权限。

下面是一些错误示例：

	# error: The requested URL returned error: 401 while accessing
	# https://github.com/user/repo.git/info/refs?service=git-receive-pack
	# fatal: HTTP request failed

	# Error: The requested URL returned error: 403 while accessing
	# https://github.com/user/repo.git/info/refs
	# fatal: HTTP request failed

	# Error: https://github.com/user/repo.git/info/refs not found: did you run git
	# update-server-info on the server?

##Check your Git version 检查 Git 版本

使用 Github 对 Git 版本没有限制，但我们发现在众多平台中  version 1.7.10 是比较稳定的版本。你最好[下载](http://git-scm.com/downloads)最新的版本。

##Ensure the remote is correct 确认远程是正确的

你要获取的库必须是存在的，并且 URL 大小写敏感。

查看本地库的 URL ,输入 `git remote -v`:

	$ git remote -v
	# View existing remotes
	# origin  https://github.com/github/reactivecocoa.git (fetch)
	# origin  https://github.com/github/reactivecocoa.git (push)

	$git remote set-url origin https://github.com/github/ReactiveCocoa.git
	# Change the 'origin' remote's URL
	
	$git remote -v
	# Verify new remote URL
	# origin  https://github.com/github/ReactiveCocoa.git (fetch)
	# origin  https://github.com/github/ReactiveCocoa.git (push)

另外,你可以在 [Mac](http://mac.github.com/) 或者 [Windows](http://windows.github.com/) 应用程序中变换 URL

##Provide access token if 2FA enabled 提供访问令牌如果 2FA 启动的话

如果启动 [2FA](https://help.github.com/articles/about-two-factor-authentication) (two-factor authentication 双因素认证),必须提供[个人访问令牌](https://help.github.com/articles/creating-an-access-token-for-command-line-use)来替换输入个人密码。

##Checking your permissions 检查权限

当输入用户名密码时，请确认这个账户是可以有权限访问库的。

*提示：如果在与库交互时，不想每次都输密码，可以[保存你的 Github 密码](https://github.com/waylau/github-help/blob/master/Caching%20your%20GitHub%20password%20in%20Git%20%E4%BF%9D%E5%AD%98%E4%BD%A0%E7%9A%84%20Github%20%E5%AF%86%E7%A0%81.md)*

如果之前已经设置了 SSH 密钥，你可以用 SSH 来代替 HTTPS 克隆 URL。更多信息，查看[该文](https://github.com/waylau/github-help/blob/master/Which%20remote%20URL%20should%20I%20use%20%E6%88%91%E5%BA%94%E8%AF%A5%E7%94%A8%E5%93%AA%E7%A7%8D%E8%BF%9C%E7%A8%8B%20URL%20.md)