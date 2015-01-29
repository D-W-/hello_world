
## git分支操作 ##
查看分支：`git branch`
创建分支：`git branch <name>`
切换分支：`git checkout <name>`
创建+切换分支：`git checkout -b <name>`
合并某分支到当前分支：`git merge <name>`
删除分支：`git branch -d <name>`
## git分支冲突 ##
两个分支同时修改了同一个文件时,会在合并的时候出现警告  
并且无法合并  
1. 使用`git status` 可以查看存在冲突的文件,这时git会用特殊标记把冲突的行标记出来  
2.  手动修改完冲突再次在master分支上面提交  
3.  这时就自动完成了两个分支的合并  
4.  使用命令`$ git log --graph --pretty=oneline --abbrev-commit`查看分支合并情况 参数`--abbrev-commit` 是为了显示的时候只显示SHA1加密得到的版本号的前几位,避免过长

## 分支管理 ##
不产生冲突的时候git默认使用fast forward合并方式,也就是直接移动指针,这样在开发过程中查看历史记录的时候有可能看不出来分支合并的情况  
使用参数`--no-ff` 解决问题,在merge的时候,这样:

    $ git merge --no-ff -m "merge with no-ff" dev
	Merge made by the 'recursive' strategy.
	readme.txt |    1 +
	1 file changed, 1 insertion(+)

使用历史记录工具查看的时候就可以看到了

    $ git log --graph --pretty=oneline --abbrev-commit
		*   7825a50 merge with no-ff
		|\
		| * 6224937 add merge
		|/
		*   59bc1cb conflict fixed
		...

> Written with [StackEdit](https://stackedit.io/).