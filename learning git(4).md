learning git(4)

git 添加远程库的时候出现错误
ssh: connect to host github.com port 22: Bad file number
ssh的端口22被关闭,原因好像是22端口不太安全
解决问题
1)继续使用ssh连接远程 换一个端口,在.ssh文件夹里面增加config文件
    C:\Users\USERNAME\.ssh\config
       Host github.com
        User git
        Hostname ssh.github.com
        PreferredAuthentications publickey
        IdentityFile ~/.ssh/id_rsa
        Port 443

 from http://stackoverflow.com/questions/7144811/git-ssh-error-connect-to-host-bad-file-number

2)改用HTTPS连接
    git clone https://github.com/username/reponame.git
    git remote add origin https://github.com/username/reponame.git

    总之就是把所有的ssh链接换成HTTPS链接就可以了

 from https://help.github.com/articles/error-bad-file-number/

