What is my disk quota 我的磁盘配额是什么
===========

GitHub 没有提供磁盘配额设置，我们尽量提供足够的存储给每个 Git 库，保证 库 尽可能的小 这样 我们给用户的服务就能更快，下载更快

##Rule of thumb: 1GB per repository, 100MB per file 经验法则：1GB每库，100MB每文件

为了获得最佳性能，我们建议每个库保持在 1GB。此限制是如果大文件（通常，编译文件）是会被清理出库的。如果你的库超过 1GB，你可能礼貌的电子邮件要求你的库的大小减少到 1GB 以下。

此外，我们将严格限制文件大小超过 100 MB。更多的信息，这是为什么，看到“[大文件的工作](https://help.github.com/articles/working-with-large-files)”

##Backups 备份

虽然听起来 Git 想是一个牛逼的备份工具，其实 Git 并不真正解决好长期备份。许多解决方案，专门设计用于执行备份比 GitHub 的微观计划甚至更便宜。

值得查看的服务，包括[ARQ](http://www.haystacksoftware.com/arq/)，[Backblaze](http://www.backblaze.com/)，[Carbonite](http://www.carbonite.com/)，[Mozy](http://mozy.com/)和[CrashPlan](http://www.crashplan.com/)。

Database dumps 数据库的转储
版本控制系统如 Git 不能很好的处理 大的 SQL 文件。如果你想为你的开发人员提供最新生产的数据集，我们建议使用 [Dropbox](https://www.dropbox.com/)的共享文件。

如果你想备份您的生产服务器，看到上面的"备份"部分。

##External dependencies 外部依赖

另一个原因的 Git 变得庞大臃肿的是外部依赖。最好把这些文件从库中移除，并使用包管理器代替，比如 最流行的 [Bundler](http://gembundler.com/), [Node's Package Manager](http://npmjs.org/) and [Maven](http://maven.apache.org/)。他们都支持直接使用 Git 仓库，这样你不需要预先打包资源。

##Packaged release versions 打包发布版本

不幸的是，Git 不善于分配编译的代码和预包装的版本。在共享大型文件的更多信息，参见“[分发大型文件](https://help.github.com/articles/distributing-large-binaries)”

##Large media files 大型媒体文件

二进制的媒体文件跟 Git 相处得不是很好。这些文件通常最好是使用一个服务。

大型媒体文件，如视频和音乐，你应该存储在自己的主机或使用服务像Vimeo 和 Youtube。

*GitHub 支持渲染设计文件比如  [PSD](https://help.github.com/articles/rendering-and-diffing-images) 和 [3D 模型](https://help.github.com/articles/3d-file-viewer)。
因为这些图形文件类型可以是非常大的，GitHub 的设计师使用 [Dropbox](https://www.dropbox.com/)保持同步。只有最终的图片形会提交到我们库。*

##Changing history of an existing repository 改变现有库的历史

如果你已经有了一个知识库，是相当大的，别担心！你可以从知识库中删除的历史大文件，减少它的大小。按照指示在“[删除敏感数据](https://help.github.com/articles/remove-sensitive-data)” 删除历史上的文件。当你这样做时，建个新的库进行测试。如果新库在磁盘的使用比原来是较小的，说明你已经成功了。


*参考：*[https://help.github.com/articles/what-is-my-disk-quota/](https://help.github.com/articles/what-is-my-disk-quota/)