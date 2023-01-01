# 1. Git 檢查相關指令
## 全檔案看差異
### git diff 
## 看單一檔案差異
### git diff [file name]

當 commit 完後，git diff 就不會再顯示之前修改的內容
而是要透過以下語法
### git show [commit id]
commit id 會顯示在你 commit 後的訊息裡，或是用 git log 做查看
## 列出檔案的每行修改紀錄(方便找出修改者)
### git blame [file name]
