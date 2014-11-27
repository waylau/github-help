What are the limits for viewing content and diffs in my repository 在版本库浏览内容和文件比较的限制是什么
===========

某些类型的资源可以很大，需要在 GitHub 做过度处理。所以会对请求做合理的限制。 

下面是常见的限制情况：

##Text limits 对本文限制

文本文件超过1 MB 总是显示为纯文本。代码不是语法高亮，并且松散格式文件不能转换为 HTML（如 Markdown, AsciiDoc 等）。

##Diff limits 对 diff 限制

diff (文件比较) 有时会变得很大，在 commit, pull , 和对比 diff 文件时将会做限制:

* 没有一个单一的文件的差异可能会超过 100 kb
* 一个比较在所有文件视图中的总大小不能超过1 MB
* 在一个单一的 diff 文件的最大数目限制为300

一个有限的差异的一些部分可能显示，但是任何超过极限的都不显示。

##Commit listings limits 表明

比较页面和 pull 请求的页会在 base 和 head 版本之间显示提交列表。这个列表限制为 500 上限，如果超过这个上限，后期提交将会记录（但不会显示）。


*参考：*[https://help.github.com/articles/what-are-the-limits-for-viewing-content-and-diffs-in-my-repository/](https://help.github.com/articles/what-are-the-limits-for-viewing-content-and-diffs-in-my-repository/)