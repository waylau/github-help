Changing a remote's URL 修改远程 URL
===========

`git remote set-url` 命令是修改存在的远程库的 URL

*提示：了解  HTTPS 和 SSH URL 的不同之处，请查看 “[我应该用哪种远程 URL](https://github.com/waylau/github-help/blob/master/Which%20remote%20URL%20should%20I%20use%20%E6%88%91%E5%BA%94%E8%AF%A5%E7%94%A8%E5%93%AA%E7%A7%8D%E8%BF%9C%E7%A8%8B%20URL%20.md)”*

这个命令带两个参数

* 已经存在远程名字，如 `origin`
* 新的远程的 URL ，如：
	* `https://github.com/USERNAME/REPOSITORY_2.git` 如果你用https 更新代码
	* `git@github.com:USER/REPOSITORY_2.git` 如果你用 SSH 更新代码

##Switching remote URLs from SSH to HTTPS 从 SSH 切换 远程 URL 到 HTTPS

1.打开终端( Mac 和 Linux 用户)或者 命令行 (Windows 用户).

2.更改当前工作路径到你的本地项目

3.列出你已经存在的远程库，为了获取到你想要修改的远程的名字

	$ git remote -v
	# origin  git@github.com:USERNAME/REPOSITORY.git (fetch)
	# origin  git@github.com:USERNAME/REPOSITORY.git (push)


4.使用 `remote set-url` 修改从 SSH 切换 远程 URL 到 HTTPS 

	$ git remote set-url origin https://github.com/USERNAME/REPOSITORY_2.git

5.验证远程URL已改变


	$ git remote -v
	# Verify new remote URL
	# origin  https://github.com/USERNAME/REPOSITORY2.git (fetch)
	# origin  https://github.com/USERNAME/REPOSITORY2.git (push)


下次，如果你使用 git fetch, git pull, 或 git push 操作库，则被要求提供账号密码

* 如果你开启[双因素认证](https://help.github.com/articles/about-two-factor-authentication)，您必须[创建一个个人访问 token](https://help.github.com/articles/creating-an-access-token-for-command-line-use) 来代替密码。
* 你可以使用一个 [credential helper](https://github.com/waylau/github-help/blob/master/Caching%20your%20GitHub%20password%20in%20Git%20%E4%BF%9D%E5%AD%98%E4%BD%A0%E7%9A%84%20Github%20%E5%AF%86%E7%A0%81.md) ，Git 会记住你的 GitHub 的用户名和密码，当每次与 GitHub 交互时。

##Switching remote URLs from HTTPS to SSH 从 HTTPS 切换 远程 URL 到 SSH

1.打开终端( Mac 和 Linux 用户)或者 命令行 (Windows 用户).

2.更改当前工作路径到你的本地项目

3.列出你已经存在的远程库，为了获取到你想要修改的远程的名字

	$ git remote -v
	# origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
	# origin  https://github.com/USERNAME/REPOSITORY.git (push)


4.使用 `remote set-url` 修改从 SSH 切换 远程 URL 到 HTTPS 

	$ git remote set-url origin git@github.com:USERNAME/REPOSITORY2.git

5.验证远程URL已改变


	$ git remote -v
	# Verify new remote URL
	# origin  git@github.com:USERNAME/REPOSITORY2.git (fetch)
	# origin  git@github.com:USERNAME/REPOSITORY2.git (push)

##Troubleshooting 故障排除

你可能会遇到这些错误时，当试图改变一个远程。

**No such remote '[name]'**

这意思是说你要修改的远程不存在

	$ git remote set-url sofake https://github.com/octocat/Spoon-Knife
	# fatal: No such remote 'sofake'

检查你是否正确地输入远程名称。

##Further reading 扩展阅读

* 《Pro Git》 书中的 "[Working with Remotes](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes)" 


*参考：*[https://help.github.com/articles/changing-a-remote-s-url/](https://help.github.com/articles/changing-a-remote-s-url/)