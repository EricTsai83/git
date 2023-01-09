# 1. Git 檢查相關指令
## 全檔案看差異
`git diff`
## 看單一檔案差異
`git diff <file name>`
## 看暫存區的所有變更
 `git diff --cached`
## 顯示工作目錄所有檔案的狀態
`git diff --name-status`
## 在儲存庫內做搜尋
`git log -S <keyword>`
## 在儲存庫內限定日期搜尋
`git log --since=<yyyy/mm/dd>  --until=<yyyy/mm/dd>`
## 在儲存庫內限定作者搜尋
`git log --author`
## 只顯示最新的 n 筆 commit
`git log -n <number>`
## 顯示樹狀結構
`git log --all --decorate --oneline --graph --color=always` 

當 commit 完後，git diff 就不會再顯示之前修改的內容
而是要透過以下語法
### git show [commit id]
commit id 會顯示在你 commit 後的訊息裡，或是用 git log 做查看
## 列出檔案的每行修改紀錄(方便找出修改者)
### git blame [file name]
