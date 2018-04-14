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
git branch 本地分支
git branch -r 遠端分支
git branch -a 所有分支
git branch <branch_name>  建立分支
git checkout <branch_name> 切換分支
git checkout -b <branch_name> 建立並切換分之
刪除分支
git branch -d <branch_name>
git branch -D <branch_name>
更名分支
git checkout master
git branch -m <old> <new>
git branch -M <old> <new>
合併分支
先切換到被合併的分支
git checkout master
git merge <branch_name>


