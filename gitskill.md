$ git config --global alias.cg "config --global" 
$ git cg alias.st status   
$ git cg alias.lgp "log --color --graph --pretty=oneline --abbrev-commit"   
$ git cg alias.lg "log --color --pretty=oneline --abbrev-commit"   
$ git cg alias.br branch   
$ git cg alias.ck checkout   
$ git cg alias.cm commit   


#Git简介
Git是目前世界上最先进的分布式版本控制系统（没有之一）。   
#安装Git
离线安装包：链接: http://pan.baidu.com/s/1gfmkGmf 密码: yast   
配置环境：win7，Microsoft.NET Framework 4.0   
#创建版本库repository
首先进入要变成Git仓库的文件夹   
初始化一个Git仓库，使用   
$ git init   
添加文件到Git仓库，分两步：   
第一步，使用命令   
$ git add <file>   
注意，可反复多次使用，添加多个文件；   
第二步，使用命令   
$ git commit -m "xxx"   
xxx为说明性文字   
#时光机穿梭
要随时掌握工作区的状态，使用   
$ git status   
如果git status告诉你有文件被修改过，用    
$ git diff
可以查看修改内容。   
##版本回退
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令  
$ git reset --hard commit_id   
$ git reset --hard head~n  
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本   
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本  
##工作区和暂存区
用git add添文件加，实际上就是把文件修改添加到暂存区；  
用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。   
##管理修改
Git跟踪并管理的是修改，而非文件
##撤销修改
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令
$ git checkout -- <file>  
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令
$ git reset HEAD <file>
回到了场景1，第二步按场景1操作。  
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
##删除文件
命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。
#远程仓库

