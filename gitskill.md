/*****���ñ���*****/
$ git config --global alias.cg "config --global" 
$ git cg alias.st status   
$ git cg alias.lgp "log --color --graph --pretty=oneline --abbrev-commit"   
$ git cg alias.lg "log --color --pretty=oneline --abbrev-commit"   
$ git cg alias.br branch   
$ git cg alias.ck checkout   
$ git cg alias.cm commit   


#Git���
Git��Ŀǰ���������Ƚ��ķֲ�ʽ�汾����ϵͳ��û��֮һ����   
#��װGit
���߰�װ��������: http://pan.baidu.com/s/1gfmkGmf ����: yast   
���û�����win7��Microsoft.NET Framework 4.0   
#�����汾��repository
���Ƚ���Ҫ���Git�ֿ���ļ���   
��ʼ��һ��Git�ֿ⣬ʹ��   
$ git init   
����ļ���Git�ֿ⣬��������   
��һ����ʹ������   
$ git add <file>   
ע�⣬�ɷ������ʹ�ã���Ӷ���ļ���   
�ڶ�����ʹ������   
$ git commit -m "xxx"   
xxxΪ˵��������   
#ʱ�������
Ҫ��ʱ���չ�������״̬��ʹ��   
$ git status   
���git status���������ļ����޸Ĺ�����    
$ git diff
���Բ鿴�޸����ݡ�   
##�汾����
HEADָ��İ汾���ǵ�ǰ�汾����ˣ�Git���������ڰ汾����ʷ֮�䴩��ʹ������  
$ git reset --hard commit_id   
$ git reset --hard head~n  
����ǰ����git log���Բ鿴�ύ��ʷ���Ա�ȷ��Ҫ���˵��ĸ��汾   
Ҫ�ط�δ������git reflog�鿴������ʷ���Ա�ȷ��Ҫ�ص�δ�����ĸ��汾  
##���������ݴ���
��git add���ļ��ӣ�ʵ���Ͼ��ǰ��ļ��޸���ӵ��ݴ�����  
��git commit�ύ���ģ�ʵ���Ͼ��ǰ��ݴ��������������ύ����ǰ��֧��   
##�����޸�
Git���ٲ���������޸ģ������ļ�
##�����޸�
����1����������˹�����ĳ���ļ������ݣ���ֱ�Ӷ������������޸�ʱ��������
$ git checkout -- <file>  
����2�����㲻�������˹�����ĳ���ļ������ݣ�����ӵ����ݴ���ʱ���붪���޸ģ�����������һ��������
$ git reset HEAD <file>
�ص��˳���1���ڶ���������1������  
����3���Ѿ��ύ�˲����ʵ��޸ĵ��汾��ʱ����Ҫ���������ύ���ο��汾����һ�ڣ�����ǰ����û�����͵�Զ�̿⡣
##ɾ���ļ�
����git rm����ɾ��һ���ļ������һ���ļ��Ѿ����ύ���汾�⣬��ô����Զ���õ�����ɾ������ҪС�ģ���ֻ�ָܻ��ļ������°汾����ᶪʧ���һ���ύ�����޸ĵ����ݡ�
#Զ�ֿ̲�
ʹ��Github  
##���Զ�̿�
ע��һ��Github  
Ҫ����һ��Զ�̿⣬ʹ������
$ git remote add origin git@Github:path/repo-name.git 
������ʹ������git push -u origin master��һ������master��֧���������ݣ�  
�˺�ÿ�α����ύ��ֻҪ�б�Ҫ���Ϳ���ʹ������git push origin master���������޸ġ�
##��Զ�̿��¡
Ҫ��¡һ���ֿ⣬���ȱ���֪���ֿ�ĵ�ַ��Ȼ��ʹ��  
$ git clone git@Github:path/repo-name.git  
Git֧�ֶ���Э�飬����https����ͨ��ssh֧�ֵ�ԭ��gitЭ���ٶ���졣
#��֧����
��֧��ƽ������
##������ϲ���֧
�鿴��֧��git branch  
������֧��git branch <name>  
�л���֧��git checkout <name>  
����+�л���֧��git checkout -b <name>  
�ϲ�ĳ��֧����ǰ��֧��git merge <name>  
ɾ����֧��git branch -d <name>
##�����ͻ(�ϲ���֧�Ż���)
��Git�޷��Զ��ϲ���֧ʱ���ͱ������Ƚ����ͻ�������ͻ�����ύ���ϲ���ɡ�  
��git log --graph������Կ�����֧�ϲ�ͼ��
##��֧�������
Git��֧ʮ��ǿ�����Ŷӿ�����Ӧ�ó��Ӧ�á�  
ͨ���ϲ���֧ʱ��Git����Fast forwardģʽ��������ģʽ�£�ɾ����֧��ᶪ����֧��Ϣ���ϲ���֧ʱ��merge�����--no-ff�����Ϳ�������ͨģʽ�ϲ����ϲ������ʷ�з�֧���ܿ��������������ϲ���
##Bug��֧
�޸�bugʱ�����ǻ�ͨ�������µ�bug��֧�����޸���Ȼ��ϲ������ɾ����  
����ͷ����û�����ʱ���Ȱѹ����ֳ�git stashһ�£�Ȼ��ȥ�޸�bug���޸�����git stash pop���ص������ֳ���
##Feature��֧
����һ����feature������½�һ����֧��  
���Ҫ����һ��û�б��ϲ����ķ�֧������ͨ��git branch -D <name>ǿ��ɾ����
##����Э��
�鿴Զ�̿���Ϣ��ʹ��git remote -v��  
�����½��ķ�֧��������͵�Զ�̣��������˾��ǲ��ɼ��ģ�  
�ӱ������ͷ�֧��ʹ��git push origin branch-name���������ʧ�ܣ�����git pullץȡԶ�̵����ύ��  
�ڱ��ش�����Զ�̷�֧��Ӧ�ķ�֧��ʹ��git checkout -b branch-name origin/branch-name�����غ�Զ�̷�֧���������һ�£�  
�������ط�֧��Զ�̷�֧�Ĺ�����ʹ��git branch --set-upstream branch-name origin/branch-name��  
��Զ��ץȡ��֧��ʹ��git pull������г�ͻ��Ҫ�ȴ����ͻ��Ȼ����push��
#��ǩ����
������ǩ
##������ǩ
����git tag <tagname>�����½�һ����ǩ��Ĭ��ΪHEAD��Ҳ����ָ��һ��commit id��  
git tag -a <tagname> -m "blablabla..." [commit id]����ָ����ǩ��Ϣ��  
git tag -s <tagname>������PGPǩ����ǩ��  
����git tag���Բ鿴���б�ǩ��  
����git show  <tagname>���Կ���˵�����֡�
##������ǩ
����git push origin <tagname>��������һ�����ر�ǩ��  
����git push origin --tags��������ȫ��δ���͹��ı��ر�ǩ��  
����git tag -d <tagname>����ɾ��һ�����ر�ǩ��  
����git push origin :refs/tags/<tagname>����ɾ��һ��Զ�̱�ǩ��
#ʹ��GitHub
��GitHub�ϣ���������Fork��Դ�ֿ⣻  
�Լ�ӵ��Fork��Ĳֿ�Ķ�дȨ�ޣ�  
��������pull request���ٷ��ֿ������״��롣
#�Զ���Git
##���������ļ�
����ĳЩ�ļ�ʱ����Ҫ��д.gitignore��  
�����ȷʵ������ļ���������add����-fǿ����ӵ�Git�� 
.gitignore�ļ�����Ҫ�ŵ��汾������ҿ��Զ�.gitignore���汾����
##���ñ���������ͷ��
$ git config --global alias.sth something  
##�Git������(����)  
