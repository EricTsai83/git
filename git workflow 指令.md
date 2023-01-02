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



# 3. Git workflow 示意圖 
[Reference](https://dev.to/mollynem/git-github--workflow-fundamentals-5496)

![git_workflow](./Img/git_workflow.png)



