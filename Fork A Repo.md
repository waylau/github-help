Fork A Repo(Fork 资源库) 
=====

fork  就是对资源库的拷贝。这样，就可以自由的修改资源库而不会对源项目造成影响。

最常见的是，fork 是用来向别人的项目做更改或使用别人的项目作为自己思想的出发点。

###向别人的项目做更改

最常用的是修改 bug 。不仅是将找到的问题记录下来，还可以：

* fork 资源库
* 做修改
* 提交 pull 请求给项目所有者

如果项目所有者喜欢你的工作，他们可能会 pull 你的修改到源资源库中。

###作为自己思想的出发点

[开源项目的核心](http://opensource.org/about)是通过分享代码，我们使软件更好，更可靠。

事实上，当你在 GitHub 上创建一个资源库，你开源选择自动包含一个 [license](http://choosealicense.com/)文件，开源用来确认你项目开源的方式。

##Fork 一个资源库的例子

只需两步，就能 Fork 一个资源库：

1.在 GitHub，切换到 [octocat/Spoon-Knife](https://github.com/octocat/Spoon-Knife) 资源库

2.在页面顶部，点击 Fork 

![](https://help.github.com/assets/images/help/repository/fork_button.jpg)

就是这样。

##保存 fork 同步

你 fork 项目，可能想修改到 upstream（上游）或 original（源） 资源库。这种情况下，最好是同步你的fork 到 upstream 资源库。

###Step 1: 安装设置 Git

如果没有，先要[设置 Git](Set Up Git.md), 不要忘了在 Git 对 Github 进行授权

###Step 2: 创建一个 fork 的本地克隆

你已经有了  Spoon-Knife 的资源库，但是没有库的文件在你的计算机上。现在创建一个  fork 的本地克隆。

1.在 Github 中，切换到 Spoon-Knife 的库。

2.右手边点击 copy 按钮复制 fork 库的 URL。

![](https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png)

3.打开终端（Mac 用户），命令行（ Windows 和 Linux 用户）

4.输入 git clone，粘贴 你复制的 URL ，就像下面，`YOUR-USERNAME` 是你的Github 的用户名。

	git clone https://github.com/YOUR-USERNAME/Spoon-Knife

5.点击 Enter, 这样你的本地克隆就创建了

	git clone https://github.com/YOUR-USERNAME/Spoon-Knife
	# Cloning into `Spoon-Knife`...
	# remote: Counting objects: 10, done.
	# remote: Compressing objects: 100% (8/8), done.
	# remove: Total 10 (delta 1), reused 10 (delta 1)
	# Unpacking objects: 100% (10/10), done.

这样，你本地就有  Spoon-Knife 的资源库了。

###Step 3: 配置 Git 用 Spoon-Knife 的源资源库来同步你的 fork

当你 fork 一个项目是为了对源资源库进行修改，那么你配置 Git 来从　original　或 upstream　资源库 pull　更改到你　fork 的本地克隆。

1.在 GitHub，切换到 [octocat/Spoon-Knife](https://github.com/octocat/Spoon-Knife) 资源库

2.右手边点击 copy 按钮复制 fork 库的 URL。

![](https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png)

3.打开终端（Mac 用户），命令行（ Windows 和 Linux 用户）

4.修改你 fork 克隆的目录
	
5.输入 `git remote -v` 点击 Enter ,你可以看到当前配置的你 fork远程库

	git remote -v
	# origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
	# origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)

6.输入 `git remote add upstream` ，接着粘贴你 Step 2 复制的 URL ，点击 Enter

	git remote add upstream https://github.com/octocat/Spoon-Knife.git

7.验证你指定 fork 新的 upstream 资源库，再次输入 `git remote -v`。你可以看到你 fork 的 URL 是 `origin`，而源资源库是`upstream`

	git remote -v
	# origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
	# origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
	# upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
	# upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)

现在你可以通过 Git 命令来在 upstream  资源库同步你的 fork。更多，详见{Syncing a fork}(Syncing a fork.md)

###下面步骤

对于 fork ，还可以做以下操作

* 创建 branch （分支）： branch 允许你构建新特性或者测试想法而不会有放入主项目的风险。
* 打开 pull 请求： 如果相对源资源库做贡献，你可以发送 [pull 请求](Using pull requests 使用 pull 请求.md)pull 你的 fork 到他们的资源库。

##寻找其他资源库来 fork 

所有公开的资源库都可以被 fork。

在[Explore GitHub](https://github.com/explore) 寻找更多精彩的项目。

![](https://help.github.com/assets/images/help/repository/fork-repo-explore.png)

##恭喜

恭喜你已经完成了 fork 的全部操作。接下来要做啥呢？

* [设置 Git](Set Up Git.md)
* [创建一个资源库](Create A Repo.md)
* Fork 一个资源库
* [加入社交](Be Social.md)


*参考*：<https://help.github.com/articles/fork-a-repo/>