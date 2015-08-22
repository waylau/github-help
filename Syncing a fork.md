Syncing a fork 同步一个 fork
====

同步 fork， 使与上游仓库保持一致。

*提示:在您同步你的 fork 和上游仓库时,您必须[配置远程指向 Git 的上游仓库](Configuring a remote for a fork.md)。*

1. 打开终端（Mac）或者命令提示符 (Windows 或者 Linux)
2. 修改当前工作目录到你本地项目
3. 获取分支和他们来自上游库的各自的提交。提交到 `master` 将会存储到本地的分支 `upstream/master`

```java

	git fetch upstream
	# remote: Counting objects: 75, done.
	# remote: Compressing objects: 100% (53/53), done.
	# remote: Total 62 (delta 27), reused 44 (delta 9)
	# Unpacking objects: 100% (62/62), done.
	# From https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY
	#  * [new branch]      master     -> upstream/master

```
4. 检出你 fork 的本地`master`分支

```java

	git checkout master
	# Switched to branch 'master'

```

5. 合并 `upstream/maste`的变化到你本地 `master`分支。这样你 fork 的  `master`会和上游仓库同步，而不会丢失你本地的变化。

```java

	git merge upstream/master
	# Updating a422352..5fdff0f
	# Fast-forward
	#  README                    |    9 -------
	#  README.md                 |    7 ++++++
	#  2 files changed, 7 insertions(+), 9 deletions(-)
	#  delete mode 100644 README
	#  create mode 100644 README.md

```

如果你本地分支没有唯一的提交，Git 将会提示 "fast-forward":

```java

	git merge upstream/master
	# Updating 34e91da..16c56ad
	# Fast-forward
	#  README.md                 |    5 +++--
	#  1 file changed, 3 insertions(+), 2 deletions(-)

```

*提示:同步你的 fork 仅更新你库的本地副本。更新在 GitHub 上 fork,你必须 [push 你的变化](Pushing to a remote.md)。*

*参考*：<https://help.github.com/articles/syncing-a-fork/>