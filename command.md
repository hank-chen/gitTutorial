git init
git config --global user.name "name"
git config --global user.email emailaddress
git status
git add filename
git commit -a -m "commits"
git log
git mv filename rename // file rename
git rm filename // delete filename
git clean -f
git reset
git branch
git branch xxx
git checkout xxx
git reset
git diff
git branch ���ط�֧
git branch -r �h�˷�֧
git branch -a ���з�֧
git branch <branch_name>  ������֧
git checkout <branch_name> �ГQ��֧
git checkout -b <branch_name> �����K�ГQ��֮
�h����֧
git branch -d <branch_name>
git branch -D <branch_name>
������֧
git checkout master
git branch -m <old> <new>
git branch -M <old> <new>
�ρ��֧
���ГQ�����ρ�ķ�֧
git checkout master
git merge <branch_name>


Git Merge
git checkout master
git merge bugfix		// fast-forward(���D)�ρ�
git merge --no-ff bugfix	// non fast-forward (�����D)�ρ�

����ָ�����Aλ��(rebase)
�ǌ�Ŀǰ��֧������׃��һ��һ������������һ����֧��
����ʹ��merge�����װl���nͻ
git checkout bugfix
git rebase master


�c�h�˜�ͨ
clone
	���h�˃�����}�u������ �K��������Ŀ��c���؃����(����.git�Y�ϊA)
pull (��ȡ)
	���h�˃��������°����d�؁� ���d�ă��ݺ���������������(object storage)
	�K�Ҍ��h�˷�֧�ρ㵽���ط�֧ (��origin/master�h�˷�֧�ρ�master���ط�֧)
push (����)
	�����؃������Ŀǰ��֧���������P������͵��h�˃������
fetch (��pull��һ�� ֻץ�Y�ϲ��ρ�)
	���h�˃�����е����°����d�؁� ���d���ݰ�����������������(object storage)

git pull = git fetch + git merage

push - ���Y�����͵�server
 Get����push�ķ�֧�c�h�˔�������fast-forward�ρ�
 ������fast-forward�ρ�����w��ǰ���ύ
 ����l���nͻpush�����ܽ^
 push���ܽ^��Ҫ�ڱ��C�Ȉ���pull(���h���µ��Y��ץ�؁� �K�ڱ��C�ρ�) pull��Ϳ���push���h��



 stash ���湦��
 �龳
	�����_�lһ���¹��� ͻȻ�gPM�؈���һ������Ҫ��BUG��Ҫ��Q ��Ŀǰ��߅�Ĺ�����δ��� ����ֱ���ͽ�(commit)
	��stash���湦�ܰѹ����^���������YӍ��������
git stash	(��׷ۙ�ęn��)
git stash -u	(������׷ۙ��δ׷ۙ)

git stash save --include-untracked -- "commit "
git stash pop


Tag ��ʹ��
�龳
	ϵ�y�_�l��һ���̶� ͨ�^��һ�A�Μyԇ����� Ҫ���N���@�汾ӛ�����
	��Tag �����ʾ�؄e�İ�̖���M��ӛ�
git tag <tagname> <commit_id>
git tag <tagname> -a -m "log message"