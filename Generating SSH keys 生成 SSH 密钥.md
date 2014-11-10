Generating SSH keys 生成 SSH 密钥
===========

*跳过本指南。直接下载我们的原生[ windows 应用程序](https://windows.github.com/)*

SSH 密钥通常用来验证计算机，而无需提供密码。本文说明了如何生成 SSH  密钥 并把它添加到你的 Github 账号。

*提示：我们建议您定期审查您的 [SSH 密钥列表](https://help.github.com/articles/keeping-your-ssh-keys-and-application-access-tokens-safe)和撤销那些没有被使用的。*

##Step 1: Check for SSH keys 检查 SSH 密钥

首先，我们需要检查您的计算机中现有的 SSH 密钥。打开你的 Git Bash 和输入：

	$ ls -al ~/.ssh
	# Lists the files in your .ssh directory, if they exist

下列为已经存在的文本：

* id_dsa.pub
* id_ecdsa.pub
* id_ed25519.pub
* id_rsa.pub

##Step 2: Generate a new SSH key 生成新的 SSH 密钥

生成一个新的SSH密钥，复制并粘贴下面的文本，确保替代你的电邮地址。默认设置是首选的，所以当你提示“Enter a file in which to save the key”，按回车继续。

	$ ssh-keygen -t rsa -C "your_email@example.com"
	# Creates a new ssh key, using the provided email as a label
	Generating public/private rsa key pair.
	Enter file in which to save the key (/c/Users/you/.ssh/id_rsa): [Press enter]

接下来，输入密码
 
*提示：我们强烈推荐使用一个很好的，安全的密码。更多信息，见 [SSH 密钥的口令工作](https://help.github.com/articles/working-with-ssh-key-passphrases)。*

	Enter passphrase (empty for no passphrase): [Type a passphrase]
	Enter same passphrase again: [Type passphrase again]

显示如下：

	Your identification has been saved in /c/Users/you/.ssh/id_rsa.
	Your public key has been saved in /c/Users/you/.ssh/id_rsa.pub.
	The key fingerprint is:
	01:0f:f4:3b:ca:85:d6:17:a1:7d:f0:68:9d:f0:a2:db your_email@example.com

添加你的新的密钥到  ssh-agent（ssh 代理）

	# start the ssh-agent in the background
	$ ssh-agent -s
	Agent pid 59566
	$ ssh-add ~/.ssh/id_rsa

##Step 3: Add your SSH key to GitHub 添加 SSH 密钥到 Github

运行下面命令，拷贝 密钥 到 剪贴板，记住 密钥 名称可能是  id_dsa.pub, id_ecdsa.pub 或 id_ed25519.pub.

	$ clip < ~/.ssh/id_rsa.pub
	# Copies the contents of the id_rsa.pub file to your clipboard

另外，使用您最喜爱的文本编辑器，你可以手动打开公共密钥文件和复制文件的内容。

现在，你有钥匙的拷贝，是时候添加到GitHub：

1. 点击右上角设置按钮![setting](https://help.github.com/assets/images/help/settings/userbar-account-settings.png);
2. 点击 **SSH keys** ![SSH KEY](https://help.github.com/assets/images/help/settings/settings-sidebar-ssh-keys.png)
3. 点击 **Add SSH key** ![add](https://help.github.com/assets/images/help/settings/ssh-add-ssh-key.png)
4. 填入 密钥的描述
5. 填入 密钥。![填入 密钥](https://help.github.com/assets/images/help/settings/ssh-key-paste.png)
6. 点击 **Add key** ![add key](https://help.github.com/assets/images/help/settings/ssh-add-key.png)
7. 确认密码

##Step 4: Test everything out 测试

打开 Git Bash 输入:

	$ ssh -T git@github.com
	# Attempts to ssh to github

看到如下警告

	The authenticity of host 'github.com (207.97.227.239)' can't be established.
	RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
	Are you sure you want to continue connecting (yes/no)?

输入 “yes”

	Hi username! You've successfully authenticated, but GitHub does not
	provide shell access.

如果 username 是你的用户名，说明你已经成功了。

如果收到”access denied（拒绝访问）“的信息。 [阅读这些问题诊断说明](https://help.github.com/articles/error-permission-denied-publickey)。

如果你从 HTTPS 转到了 SSH ，需要更新你的 远程库的 URL。请参阅[转换远程URL](https://help.github.com/articles/changing-a-remote-s-url)


*参考*：[https://help.github.com/articles/generating-ssh-keys/](https://help.github.com/articles/generating-ssh-keys/)
