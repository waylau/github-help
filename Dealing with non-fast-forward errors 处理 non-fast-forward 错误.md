Dealing with non-fast-forward errors 处理 non-fast-forward 错误
===========

有时候 Git 在没有 commit 时，不能提交修改到远程库。此时， 你的 push  将会被拒绝。

如果另外一个人像你一样 提交 到了相同的 分支， Git 不让你提交你的change （变化）:

	$ git push origin master
	# To https://github.com/USERNAME/REPOSITORY.git
	#  ! [rejected]        master -> master (non-fast-forward)
	# error: failed to push some refs to 'https://github.com/USERNAME/REPOSITORY.git'
	# To prevent you from losing history, non-fast-forward updates were rejected
	# Merge the remote changes (e.g. 'git pull') before pushing again.  See the
	# 'Note about fast-forwards' section of 'git push --help' for details.

可以在本地通过  fetch（获取） 与 merge （合并）  相同的分支的  change （变化） 来解决:

	$ git fetch origin
	# Fetches updates made to an online repository
	$ git merge origin branch
	# Merges updates made online with your local work

可以简单使用`git pull` 提交:

$ git pull origin branch
# Grabs online updates and merges them with your local work