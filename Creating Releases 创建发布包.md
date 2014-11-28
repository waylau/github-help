Creating Releases 创建发布包
===========

发布包是让用户接触项目不错的方式：

1.页面顶端，点击你的用户名

![](https://help.github.com/assets/images/help/profile/top_right_avatar.png)

2.在你的 profile  页面，点击 Repositories 窗口，接着点击你的库的名称

![](https://help.github.com/assets/images/help/profile/profile_repositories_tab.png)

3.顶端，点击 releases

![](https://help.github.com/assets/images/help/releases/releases-header-menu.png)

4.点击 Draft a new release

![](https://help.github.com/assets/images/help/releases/draft_release_button.png)

5.输入发布包的版本号。版本号基于 [Git 标签](http://git-scm.com/book/en/Git-Basics-Tagging),我们建议标签命名，符合[语义版本](http://semver.org/)。

![](https://help.github.com/assets/images/help/releases/releases_tag_version.png)

6.选择一个分支来包含你想发布的项目。通常，你会想发布在你的主分支，除非你发布测试软件。

![](https://help.github.com/assets/images/help/releases/releases_tag_branch.png)

7.在你的发布包中输入标题和描述

![](https://help.github.com/assets/images/help/releases/releases_description.png)

8.如果发布中包含二进制文件，托文件进二进制框中

![](https://help.github.com/assets/images/help/releases/releases_adding_binary.gif)


9.如果，发布包不稳定，选择`This is a pre-release` 来提醒用户这个是不能用于生产环境的

![](https://help.github.com/assets/images/help/releases/prerelease_checkbox.png)


10.如果准备好了发布了，点击 Publish release。另外 点击 Save draft 用于保存在草稿箱中。只有你和[你的合作者]()可以看到到草稿箱。

![](https://help.github.com/assets/images/help/releases/release_buttons.png)


##Automatically creating releases 自动创建发布

 自动创建发布（支持命令行或者脚本），详见[Releases API documentation.](https://developer.github.com/v3/repos/releases/#create-a-release)

##Further reading 扩展阅读

* [链接到发布包]()



参考：[https://help.github.com/articles/creating-releases/](https://help.github.com/articles/creating-releases/)
