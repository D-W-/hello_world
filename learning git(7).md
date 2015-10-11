
## 保存现场 ##
git里面需要停下手头没完成的工作去操作另一个分支的时候,就需要把自己现在的分支先保存一下,也就是把现在的头指针保存一下,然后转移指针到和master分支同步的地方,应该是放到了一个栈里面..要不命令里面为啥会有pop..

 1. 保存现场 `git stash`
 2. 恢复现场 `git stash pop`  
     或者 `git stash apply`  
     然后 `git stash drop`
 3. 查看当前保存了那些现场 `git stash list`

## 丢弃一个分支 ##

 1. 分支已经被合并了 直接 `git branch -d <name>` 就可以了
 2. 分支没有被合并 `git branch -D <name>`

> Written with [StackEdit](https://stackedit.io/).