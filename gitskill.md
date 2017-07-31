/*****设置别名*****/     
$ git config --global alias.cg "config --global"  
$ git cg alias.st status   
$ git cg alias.lgp "log --color --graph --pretty=oneline --abbrev-commit"   
$ git cg alias.lg "log --color --pretty=oneline --abbrev-commit"   
$ git cg alias.br branch   
$ git cg alias.ck checkout   
$ git cg alias.cm commit   
$ git cg alias.pp "push origin"


# Git简介
Git是目前世界上最先进的分布式版本控制系统（没有之一）。   

# 安装Git
离线安装包：链接: http://pan.baidu.com/s/1gfmkGmf 密码: yast   
配置环境：win7，Microsoft.NET Framework 4.0 

# 创建版本库repository
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
  
# 时光机穿梭
要随时掌握工作区的状态，使用   
$ git status   
如果git status告诉你有文件被修改过，用    
$ git diff
可以查看修改内容。
 
## 版本回退
HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令  
$ git reset --hard commit_id   
$ git reset --hard head~n  
穿梭前，用git log可以查看提交历史，以便确定要回退到哪个版本   
要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本  

## 工作区和暂存区
用git add添文件加，实际上就是把文件修改添加到暂存区；  
用git commit提交更改，实际上就是把暂存区的所有内容提交到当前分支。

## 管理修改
Git跟踪并管理的是修改，而非文件

## 撤销修改
场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令
$ git checkout -- <file>  
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令
$ git reset HEAD <file>
回到了场景1，第二步按场景1操作。  
场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。
  
## 删除文件
命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。

# 远程仓库
使用Github  

## 添加远程库
注册一个Github  
要关联一个远程库，使用命令
$ git remote add origin git@Github:path/repo-name.git 
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；  
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改。

## 从远程库克隆
要克隆一个仓库，首先必须知道仓库的地址，然后使用  
$ git clone git@Github:path/repo-name.git  
Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快。

# 分支管理
分支就平行世界

## 创建与合并分支
查看分支：git branch  
创建分支：git branch <name>  
切换分支：git checkout <name>  
创建+切换分支：git checkout -b <name>  
合并某分支到当前分支：git merge <name>  
删除分支：git branch -d <name>
  
## 解决冲突(合并分支才会有)
当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，合并完成。  
用git log --graph命令可以看到分支合并图。

## 分支管理策略
Git分支十分强大，在团队开发中应该充分应用。  
通常合并分支时，Git会用Fast forward模式，但这种模式下，删除分支后会丢掉分支信息。合并分支时在merge后加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并。

## Bug分支
修复bug时，我们会通过创建新的bug分支进行修复，然后合并，最后删除；  
当手头工作没有完成时，先把工作现场git stash一下，然后去修复bug，修复后，再git stash pop，回到工作现场。

## Feature分支
开发一个新feature，最好新建一个分支；  
如果要丢弃一个没有被合并过的分支，可以通过git branch -D <name>强行删除。
  
## 多人协作
查看远程库信息，使用git remote -v；  
本地新建的分支如果不推送到远程，对其他人就是不可见的；  
从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；  
在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；  
建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；  
从远程抓取分支，使用git pull，如果有冲突，要先处理冲突，然后再push。
  
# 标签管理
类似书签

## 创建标签
命令git tag <tagname>用于新建一个标签，默认为HEAD，也可以指定一个commit id；  
git tag -a <tagname> -m "blablabla..." [commit id]可以指定标签信息；  
git tag -s <tagname>可以用PGP签名标签；  
命令git tag可以查看所有标签；  
命令git show  <tagname>可以看到说明文字。
  
## 操作标签
命令git push origin <tagname>可以推送一个本地标签；  
命令git push origin --tags可以推送全部未推送过的本地标签；  
命令git tag -d <tagname>可以删除一个本地标签；  
命令git push origin :refs/tags/<tagname>可以删除一个远程标签。
  
# 使用GitHub
在GitHub上，可以任意Fork开源仓库；  
自己拥有Fork后的仓库的读写权限；  
可以推送pull request给官方仓库来贡献代码。

# 自定义Git

## 忽略特殊文件
忽略某些文件时，需要编写.gitignore；  
如果你确实想添加文件，可以在add后用-f强制添加到Git； 
.gitignore文件本身要放到版本库里，并且可以对.gitignore做版本管理！

## 配置别名（见开头）
$ git config --global alias.sth something  

## 搭建Git服务器(跳过)  
