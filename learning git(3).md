learning git(3)

文件删除问题,当一个文件在本地被删除了,但是已经提交到了git上面

可以
    1.用版本库中的版本进行恢复
    $ git checkout -- test.txt
    版本库中的版本是你提交到git上的最新版本,只要是add的内容都会恢复,即使没有commit,但是没有add,只在本地修改的内容不能恢复..

    2.确实要删掉那个文件的话
    $ git rm test.txt
    rm 'test.txt'
    $ git commit -m "remove test.txt"

