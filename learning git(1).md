learning git(1)

为什么Git添加文件需要add，commit一共两步呢？因为commit可以一次提交很多文件，所以你可以多次add不同的文件，比如：

$ git add file1.txt
$ git add file2.txt
$ git add file3.txt
$ git commit -m "add 3 files."

$ git status
--查看当前状态

$ git diff readme.txt
--查看当前文件(readme.txt)修改了什么内容

$ git log
--查看提交历史，以便确定要回退到哪个版本。
$ git log --pretty=oneline
一行显示,前面是SHA1的值,后面是commit时写的修改信息

$ git reflog
--查看命令历史，以便确定要回到未来的哪个版本。

$ git reset --hard commit_id
--回退到 commit_id 版本
commit_id 的取值
1) HEAD 代表当前版本 HEAD^代表上一个版本
2) 可以直接用每次commit的SHA1值,具体的值可以用git reflog或git log查看

