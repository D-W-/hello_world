
## git远程库的关联 ##
要关联一个远程库，使用命令`git remote add origin git@server-name:path/repo-name.git`；

关联后，使用命令`git push -u origin master`第一次推送master分支的所有内容；

此后，每次本地提交后，只要有必要，就可以使用命令`git push origin master`推送最新修改；

## git从远程库clone项目 ##

    git clone git@github.com:michaelliao/gitskills.git

> Written with [StackEdit](https://stackedit.io/).