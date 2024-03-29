### vscode
- ctrl+shift+p (開啟設定)
	-  選擇Default
		- Terminal cmd

### 版本號檢視
- git --version

### 建立全域端使用者
- git config --global user.name xxx
- git config --global user.email xxx@gmail.com

### 檢視git設定
- git config --list

### 控管專案
- git init

### 檔案加入控管
- git add <filename>
	- Untrack => Added => Modified =>Deleted   

### 檢視控管狀態
- git status

### 檢視物件內容(t:型態,p:內容)
- git cat-file -t sha1 
- git cat-file -p sha1

### Added=>Modified 
- git status
- git add filename (確認修改)

### 反悔修改
- git restore filename

### 檢視暫時儲存區目前內容
- git ls-files -s

### 記錄到倉庫
- git commit -m "message"
- git commit -am "message"
	- a=>add
	
### 檢視目前commit 
- git log 
- git log --oneline 

### 開啟vim編輯器(linux)
-   git commit 
	- i (Insert)
	- esc切換功能 
		- :wq (儲存後離開)
		- :q! (直接離開)

### 合併上一次commit (不新增commit)
- git commit --amend


### 刪除指令
- git rm -f filename (強制刪除)
	- git restore --staged filename (恢復)

### 將檔案移出(暫存/倉庫)
- git rm --cached filename

### 檢視分支
- git branch 
	- 預設為master分支(需有commit才會出現)

### 新增分支
- git branch test

### 切換分支
- git checkout test

### 新增+切換分支
- git checkout -b dev

### 合併分支
- git checkout master(切回主分支)
	- git merge test

### 刪除分支
- git branch -D test

### 切換commit
- git checkout commit-sha1
- 回到過去的修正
 	- 新增分支跟commit 
	- 切回master進行合併
- 回到最新位置
	- git checkout master

### 合併衝突
- 不同分支改動同一個檔案(選擇合併方式)
- git merge --abort (反悔合併)

###　重置指令
- git reset commit-sha1
- git reset --hard commit-sha1
- git reset ORIG_HEAD (恢復動作）
- git reset --hard HEAD (重置到最新的commit)
- git reset --hard HEAD~1 (重置到最新的commit的前一個) 

### 檢視所有歷程
- git reflog
	- 可以觀察commit-shal，進行reset(重置指令)
-----------------------------------------
### github
- echo "# Git-demo" >> README.md
- git init
- git add README.md
- git commit -m "first commit"
- git branch -M main
- git remote add origin https://github.com/Danielready1103/Git-demo.git
- git push -u origin main

###綁定雲端倉庫
- git remote add origin https://github.com/Danielready1103/Git-demo.git
- git remote -v
	- 檢視綁定的雲端倉庫url

###同步到雲端
- git push (第二次開始直接使用此指令即可)
	- git push --set-upstream origin master (第一次要使用此指令，以此建立分支)
	- git push -u origin main
	- git push 

### 複製專案
- git clone https://github.com/Danielready1103/Git-demo

###雲端同步到本地端
- git pull
