Distributing large binaries 分发大型二进制文件.
===========

当项目需要分发大型的文件，比如 二进制文件或者安装包时，有几种廉价方式提供大容量存储和分发大型文件。

我们推荐在 Github 上 创建[项目的发布包](https://github.com/waylau/github-help/blob/master/About%20Releases%20%E5%85%B3%E4%BA%8E%E5%8F%91%E5%B8%83%E5%8C%85.md)。发布包允许包括二进制文件，比如编译后的程序。更多信息，参阅[创建发布包](https://github.com/waylau/github-help/blob/master/Creating%20Releases%20%E5%88%9B%E5%BB%BA%E5%8F%91%E5%B8%83%E5%8C%85.md)。

暂时，我们没有在二进制文件的大小和上传带宽做任何限制。

##Using Amazon S3 使用 AS3

或者，您可以使用 [Amazon S3](http://aws.amazon.com/s3/)存储服务，搭配通过 CloudFront 的 CDN 。亚马逊有一个不错的用户指南 [ Getting started with S3 ](http://docs.amazonwebservices.com/AmazonS3/latest/gsg/GetStartedWithS3.html)，介绍了如何上传文件。

如果你是 OS X 操作系统， [Transmit](http://panic.com/transmit/) 和 [3hub](http://www.3hubapp.com/) 是两个流行的客户端 。

如果你是 Windows 操作系统, [S3 Browser](http://s3browser.com/) 是个不错的管理 AS3 文件的免费应用。

当你上传完成后，可以插入链接到 	`README` 或者库的描述文档中。


参考：[https://help.github.com/articles/distributing-large-binaries/](https://help.github.com/articles/distributing-large-binaries/)
