# 1. Git workflow 相關指令
## 設定主機的 git 使用者名稱及電子信箱
###  git config --global user.name "kewang"
### git config --global user.email "eric492718@gmail.com"
## git 初始化
### git init
## git 保管狀態
### git status
## 將檔案放入 git 內，準備被保管
### 單一檔案加到 git 中保管: git add [file]
### 所有檔案加到 git 中保管: git add .
## 將被 git 保管的檔案送出，並同時提供註解
### git commit -m "first time commit"
## 註解會顯示在 log 上
### git log => 會進到 log 裡面，退出按 q

# 2. 檔案操作情境
## 刪除檔案
### rm [file]
### git status
### git add [file] or git rm [file] => the same thing
### git commit -m "remove the file"
## 變更檔名
### mv file_name new_file_nameß
### git add new_file_name
### git commit -m "rename the file"

# 3. Git workflow 示意圖
![git_workflow](./Img/git_workflow.png)
