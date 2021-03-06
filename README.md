# LearnGitHub
学习使用gitHub

## 熟悉常用的git命令

* 初始化一个git仓库

	- 新建文件夹，在终端中打开，然后执行 `git init`
	
* clone一个git仓库

	- 新建文件夹，在终端中打开，然后执行 `git clone [repositoryPath]` 
	
* 把修改的文件添加到暂存区域
	
	- 执行 `git add [filename]` 添加一个文件
	- 或执行 `git add *` 添加所有文件
	- 或执行 `git add .` 添加当前文件夹下的所有文件

* 把修改并暂存的文件提交到本地仓库

	- 执行 `git commit -m "文件改动信息"`	提交所有暂存文件
	- 或者执行 `git commit -m "文件改动信息" [fileName]` 提交指定暂存文件

* 使用命令行提交项目并push到github仓库
 
	- 执行 `git push origin [branchName]` 把指定分支push到远程服务器

* 新建的仓库一般没有连接到远程的服务器

	- 执行 `git remote add origin [server]` 来连接远程服务器

* 分支是用来把不同的开发方向骤隔离开来，防止冲突，等开发工作完成之后再合并到主分支上
	
	- 执行 `git branch` 查看已有分支
	- 执行 `git branch [branchName]` 新建分支
	- 执行 `git checkout [branchName]` 切换分支
	- 执行 `git checkout -b [branchName]` 新建分支并切换到分支
	- 执行 `git branch -d [branchName]` 删除指定分支
	

* 每次工作前建议先同步一下当前分支的文件，保持文件最新，以便于减少与他人提交文件的冲突可能性。
	
	- 执行 `git pull` 获取最新改动并合并
	- 执行 `git fetch [branchName]` 获取远端分支最新改动
	- 执行 `git merge [branchName]` 把远端分支最新改动合并到当前分支
	
* 替换本地文件
	- 执行 `git checkout -- [fileName]` 撤销文件改动



***

## 熟悉常用的[MarkDown](http://www.jianshu.com/p/1e402922ee32/)语法
> Markdown 可谓是十分轻量的，学习成本也不需要太多，且一旦熟悉这种语法规则，会有一劳永逸的效果。

##### **MarkDown使用起来真的很方便**

* 标题

标识符：#

* 列表

标识符：-,*,1. 2. 

* 链接

标识符:使用英文的【】(xxxxx)

* 引用

标识符：>xxxxxxx

* 粗体、斜体

粗体标识符：使用**包裹的内容
斜体标识符：使用*包裹的内容

***
##使用ssh验证的时候容易出现的问题
-在git客户端切换账号的时候，容易出现账号切换了，但是使用的ssh private key 没有更改的问题

解决办法：

查看已经添加的证书：'ssh-add -l'

删除所有的证书：'ssh-add -D'

删除指定路径的证书： 'ssh-add -d xxxpath'
添加指定证书：'ssh-add xxxpath'
