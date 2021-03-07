What happens to forks when a repository is deleted or changes visibility 当库删除或者改变了可见性,其 fork 发生了什么
===========

本文介绍了删除你的库或改变其可见性对于这个库的 fork 们的影响。

## Deleting a private repository 删除私人库

当删除私人库，其私人 fork 也都删除

## Deleting a public repository 删除公开库

你删除一个公开库时，一个现有的公开 fork 被选为新的父库。所有其他库都会是这个父库的 fork,随后的请求发到到这个新的父库。

换句话说，一个公开库的 fork 将保持在自己单独的库网络是公开的，即使父库是私有的。这允许 fork 业主们继续合作无间。如果公开 fork 不进入这样一个单独的网络，这些 fork 业主需要得到适当的访问权限来提交变化和请求到（现在是私人）父库，即使在之前他们并不需要这些权限。

### Deleting the private repository 删除私人库

如果一个公开库是私有的，然后删除，其公共 fork 将继续在一个单独的网络存在。

## Changing a private repository to a public repository 将私人库转为公开

如果一个私人库变为公开的，它的每一个私有 fork 变成一个独立的私人仓库,并成为自己的新库母网络。私人 fork 不会自动公开，因为他们可能包含敏感的提交，不应该公开暴露。

如果你拥有一个私人 fork 已被转换成一个独立的私人库，你将要买单。这只私人 fork 是免费的。如果你不签了一份支付计划，或者如果你没有一个房间在你当前的计划给其他私人库，库将被锁定。您必须升级或切换为公开库。（你可以随时[更改库为公开](https://github.com/waylau/github-help/blob/master/Making%20a%20private%20repository%20public%20%E7%A7%81%E4%BA%BA%E5%BA%93%E8%BD%AC%E4%B8%BA%E5%85%AC%E5%BC%80.md)）

更多关于当库被锁时发生了什么，请参见“[https://github.com/waylau/github-help/blob/master/What%20happens%20if%20my%20repository%20is%20locked%20%E5%BD%93%E5%BA%93%E9%94%81%E4%BD%8F%E6%97%B6%E5%8F%91%E7%94%9F%E4%BA%86%E5%95%A5.md](https://github.com/waylau/github-help/blob/master/What%20happens%20if%20my%20repository%20is%20locked%20%E5%BD%93%E5%BA%93%E9%94%81%E4%BD%8F%E6%97%B6%E5%8F%91%E7%94%9F%E4%BA%86%E5%95%A5.md)”

### Deleting the public repository 删除公开库

如果一个私有库转为公开的，然后删除，其私人 fork 将继续作为独立的私人库在单独的网络存在

参考：[https://help.github.com/articles/what-happens-to-forks-when-a-repository-is-deleted-or-changes-visibility/#changing-a-public-repository-to-a-private-repository](https://help.github.com/articles/what-happens-to-forks-when-a-repository-is-deleted-or-changes-visibility/#changing-a-public-repository-to-a-private-repository)
