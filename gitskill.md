$ git config --global alias.cg "config --global" 
$ git cg alias.st status   
$ git cg alias.lgp "log --color --graph --pretty=oneline --abbrev-commit"   
$ git cg alias.lg "log --color --pretty=oneline --abbrev-commit"   
$ git cg alias.relgp "relog --color --graph --pretty=oneline --abbrev-commit"   
$ git cg alias.relg "relog --color --pretty=oneline --abbrev-commit"   

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
