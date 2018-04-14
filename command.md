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


Git Merge
git checkout master
git merge bugfix		// fast-forward(快轉)合併
git merge --no-ff bugfix	// non fast-forward (不快轉)合併

重新指定基礎位置(rebase)
是將目前分支的所有變更一個一個的套用在另一個分支上
會比使用merge更容易發生衝突
git checkout bugfix
git rebase master


與遠端溝通
clone
	將遠端儲存庫複製到本地 並建立工作目錄與本地儲存庫(就是.git資料夾)
pull (拉取)
	將遠端儲存庫的最新版下載回來 下載的內容含完整的物件儲存庫(object storage)
	並且將遠端分支合併到本地分支 (將origin/master遠端分支合併master本地分支)
push (推送)
	將本地儲存庫中目前分支的所有相關物件推送到遠端儲存庫中
fetch (是pull的一半 只抓資料不合併)
	將遠端儲存庫中的最新版下載回來 下載內容包含完整的物件儲存庫(object storage)

git pull = git fetch + git merage

push - 將資料推送到server
 Get會把push的分支與遠端數據庫以fast-forward合併
 若不是fast-forward合併會覆蓋以前的提交
 如果發生衝突push會被拒絕
 push被拒絕就要在本機先執行pull(把遠端新的資料抓回來 並在本機合併) pull後就可以push回遠端



 stash 暫存功能
 情境
	正在開發一個新功能 突然間PM回報有一個很重要的BUG需要解決 但目前手邊的工作尚未完成 不能直接送交(commit)
	用stash暫存功能把工作區及索引的資訊暫存起來
git stash	(已追蹤的檔案)
git stash -u	(包含已追蹤及未追蹤)

git stash save --include-untracked -- "commit "
git stash pop


Tag 的使用
情境
	系統開發到一定程度 通過第一階段測試及驗收 要怎麼把這版本記錄起來
	用Tag 工來標示特別的版號或進行記錄
git tag <tagname> <commit_id>
git tag <tagname> -a -m "log message"