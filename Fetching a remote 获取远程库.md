
Fetching a remote 获取远程库
===========

当与其他人的库进行交互时，需记住下面几个 Git 命令：

* git clone
* git fetch
* git merge
* git pull

上述命令对于跟[远程库](https://help.github.com/articles/about-remote-repositories)交互非常有用。`clone` 和 `fetch`是通过库的 URL 来下载远程库源码到你本地的计算机。 `merge` 是合并不同人的工作到你的工作中。`pull` 是 `fetch` 和 `merge`的结合。

下面详述命令：

##Clone 复制

复制人家的库，用 `git clone`

	$ git clone https://github.com/USERNAME/REPOSITORY.git
	# Clones a repository to your computer

你可以选[不同的 URL](https://github.com/waylau/github-help/blob/master/Which%20remote%20URL%20should%20I%20use%20%E6%88%91%E5%BA%94%E8%AF%A5%E7%94%A8%E5%93%AA%E7%A7%8D%E8%BF%9C%E7%A8%8B%20URL%20.md) 来复制 库。当登录系统，可以看到：

![##Clone ](https://help.github.com/assets/images/help/repository/remotes-url.png)

当执行 `git clone`,发生下面动作
* 新的文件夹 `repo`生成
* 被初始化成一个 Git 库
* 远程库名 `origin` 被生产，执行了你所复制的 URL
* 所有的 库的文件 和提交 都被下载下来
* 默认 分支 (通常为 `master`) 被检出

在远程库中的所有 foo 分支，相应的远程跟踪分支`refs/remotes/origin/foo`已经创建在你的本地库。通常你可以把这样的远程跟踪分支的命名为 `origin/foo`

##Fetch

`git fetch` 是用来人家新的工作内容。获取远程库上的新的跟踪是不需要处理合并变化的。

如果你已经有一个本地仓库与[远程URL](https://help.github.com/articles/adding-a-remote)设置为所需的项目，你可以获取所有新的信息通过使用 `git fetch * RemoteName *`：

	$ git fetch remotename
	# Fetches updates made to a remote repository

否则，你可以添加一个[新的远程](https://help.github.com/articles/adding-a-remote)然后获取。

##Merge

Merge 是用来合并你的本地变化和其他人制作的变化。

通常，你合并远程跟踪分支（比如，一个从远程库获取的分支）到你的本地分支中
​	
	$ git merge remotename/branchname
	# Merges updates made online with your local work

##Pull

`git pull` 是一个快捷的 实现 `git fetch` 和 `git merge` 相同的命令

	$ git pull remotename branchname
	# Grabs online updates and merges them with your local work

因为 `pull` 执行合并对检索到的变化，你应该确保你的工作在 `pull` 之前是 `commit` 的。如果你遇到一个[合并冲突](https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line)无法解决，或如果你决定退出合并，你可以用 `git merge --abort` 来返回。

##Further reading 扩展阅读

* Pro Git 书中的 ["Working with Remotes"](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes)
* [GitGuys: Adding and Removing Remote Branches](http://www.gitguys.com/topics/adding-and-removing-remote-branches/)
