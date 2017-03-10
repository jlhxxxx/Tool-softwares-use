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
