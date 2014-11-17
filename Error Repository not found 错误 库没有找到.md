Error:Repository not found 错误 库没有找到
===========

如果你在拷贝项目库时看到这个提示错误，说明库已经不在了或者你没有访问权限。解决方法如下：

##Check your spelling 检查拼写

名字拼错很常见，比如 你拷贝 `git@github.com:user/repo.git`的项目库， 但是 真是的库名可能是 `User/Repo`,你会收到这样的错误。

为了避免这类错误，你直接拷贝 URL 得了，别手打。

![url](https://help.github.com/assets/images/help/repository/https-url-clone.png)

更新存在的远程库，请移步至“[更改远程 URL](https://help.github.com/articles/changing-a-remote-s-url)”

##Checking your permissions 检查你的权限

你想拷贝一个私人的库，但是如果没有访问权限，同样你会收到这个错误。

确认你的访问权限：

* 库的主人
* 在库的[合作伙伴](https://help.github.com/articles/adding-collaborators-to-a-personal-repository)
* 一个团队的成员可以访问该库（如果库属于一个组织）

##Check your SSH access 检查你的 SSH 访问

罕见的情况下，您可能没有适当的SSH访问一个版本库。

你必须确保你使用 SSH 密钥连接到你的 GitHub 的用户帐户。你可以通过在命令行键入如下：

	$ ssh -T git@github.com
	# Hi username! You've successfully authenticated, but GitHub does not
	# provide shell access.

更多信息，参见[生成 SSH 密钥](https://github.com/waylau/github-help/blob/master/Generating%20SSH%20keys%20%E7%94%9F%E6%88%90%20SSH%20%E5%AF%86%E9%92%A5.md)

##Check that the repository really exists 检查库是否真实存在

如果一切都失败了，请确保在 GitHub 库真的存在！如果你想提交代码到一个不存在的库，你会得到这个错误。

*参考：*[https://help.github.com/articles/error-repository-not-found/](https://help.github.com/articles/error-repository-not-found/)