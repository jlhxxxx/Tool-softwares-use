$ git config --global alias.cg "config --global" 
$ git cg alias.st status   
$ git cg alias.lgp "log --color --graph --pretty=oneline --abbrev-commit"   
$ git cg alias.lg "log --color --pretty=oneline --abbrev-commit"   
$ git cg alias.relgp "relog --color --graph --pretty=oneline --abbrev-commit"   
$ git cg alias.relg "relog --color --pretty=oneline --abbrev-commit"   

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
