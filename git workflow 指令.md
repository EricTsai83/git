# 1. Git workflow 相關指令
## 設定主機的 git 使用者名稱及電子信箱
* git config --global user.name "XXXXXX"
* git config --global user.email "XXXXXXX@gmail.com"

## git 初始化
* git init

## git 保管狀態
* git status

## 將檔案放入 git 內，準備被保管
* 單一檔案加到 git 中保管: git add [file]
* 所有檔案加到 git 中保管: git add .

## 將被 git 保管的檔案送出，並同時提供註解
* git commit -m "first time commit"

## 註解會顯示在 log 上
* git log => 會進到 log 裡面，退出按 q

# 2. 檔案操作情境
## 刪除檔案
1. rm [file]
2. git status
3. git add [file] or git rm [file] => the same thing
4. git commit -m "remove the file"

## 變更檔名
1. mv file_name new_file_nameß
2. git add new_file_name
3. git commit -m "Rename the file"

# 3. 透過 checkout 進行檔案變更
`git checkout <sha1>`

* 將儲存庫內 sha1 版本的所有資料取出至工作目錄 (HEAD)
* 工作目錄會移到 sha1

`git checkout head`

* 將儲存庫內 HEAD 版本的所有資料取出至工作目錄 (HEAD)
* 工作目錄會移到 (HEAD) => 無作用(工作目錄本來就在 HEAD)

`git checkout <sha1> <file>` or `git checkout <sha1> .`

* 將儲存庫內 sha1 版本的 file 取出至現在的工作目錄(HEAD)
* 工作目錄的 file 會變成 sha1 版本的

` git reset --hard <sha1>`

* 將工作目錄回復到 sha1 下的狀態 

`git checkout HEAD <file>` or `git checkout -- <file>`
 
`git checkout HEAD .` or `git checkout -- .`

* 將儲存庫內 HEAD 版本的 file 取出至工作目錄
* 讓工作目錄的 file 變成 HEAD 版本的 (目的是用來還原用的。前提是你沒有做 git add 的動作)

# 4. 將工作拆分成可同時進行的分支
`git branch <branchname>`

* 將工作目錄 (HEAD) 新增一個分支，名為 <branchname>

`git branch <bn> <sha1>`

* 將 sha1 新增一個分支，名為 bn

`git branch -D <branchname>`

* 刪除名為 branchname 的分支(只是刪除名稱而已，對檔案沒有影響)

`git checkout <branchname>`

* 將儲存庫內名為 branchname 分支的所有資料取出至工作目錄 (HEAD)
* 工作目錄會移至 branchname

`git merge <branchname>`

* 合併已經完成的分支

* 將 branchname 分支合併到工作目錄 (HEAD)

# 5. 解決分支合併時的檔案衝突(相同檔案再不同分支有不同的狀態)
`git merge --abort` 

* 取消合併

`git commit`

* 修改其中一邊分支的檔案讓它與另一邊分支的檔案一致，然後再打上 commit 語法

# 6. 將某 commit 獨立插入其他分支
通常是把已發布的分支修正 bug 之後，把同一個 bug 也在其他分支中修復

`git cherry-pick <sha1>`

* 將 sha1 or branchname 的 commit 作為現在這個分支 HEAD 新的 commit

# 7.Git workflow 示意圖 
[Reference](https://dev.to/mollynem/git-github--workflow-fundamentals-5496)

![git_workflow](./Img/git_workflow.png)



