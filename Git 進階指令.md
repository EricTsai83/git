# Git 進階指令
## 列出所有分支
`git branch -av`: 詳細
`git branch -a`: 簡單

## 遠端分支
### 設定遠端分支
 `git branch --set-upstream-to=orign/<遠端分支名稱> <本機分支名稱>`
### 刪除遠端分支(常常用在忘了刪除功能分支)
`git push orign : <遠端分支名稱>`
### 刪除已經沒有遠端分支的遠端追蹤分支
`git remote prune origin`

## 其他進階語法
[git-extras](https://github.com/tj/git-extras)