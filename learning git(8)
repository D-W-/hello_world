多人协作
----
多人协作的工作模式通常是这样：

 1. 首先，可以试图用`git push origin branch-name`推送自己的修改；

 2. 如果推送失败，则因为远程分支比你的本地更新，需要先用`git pull`试图合并；

 3. 如果合并有冲突，则解决冲突，并在本地提交；

 4. 没有冲突或者解决掉冲突后，再用`git push origin branch-name`推送就能成功！

 5. 如果`git pull`提示“no tracking information”，则说明本地分支和远程分支的链接关系没有创建，用命令`git branch --set-upstream branch-name origin/branch-name`。

这就是多人协作的工作模式，一旦熟悉了，就非常简单。

## 标签管理 ##

标签是版本库的一个快照  
实际上是指向某个commit的指针,const 指针,因为标签不可以改变

 - 命令`git tag <name> <commit id>`用于新建一个标签，默认为HEAD，也可以指定一个commit id；

 - `git tag -a <tagname> -m "blablabla..."`可以指定标签信息；

 - `git tag -s <tagname> -m "blablabla..."`可以用PGP签名标签；

 - 命令`git tag`可以查看所有标签。 
 
 - 用命令`git show <tagname>`可以看到说明文字  
 
 - 命令`git push origin <tagname>`可以推送一个本地标签；

 - 命令`git push origin --tags`可以推送全部未推送过的本地标签；

 - 命令`git tag -d <tagname>`可以删除一个本地标签；

 - 命令`git push origin :refs/tags/<tagname>`可以删除一个远程标签。

> Written with [StackEdit](https://stackedit.io/).