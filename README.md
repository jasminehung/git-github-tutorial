# Git & Github tutorial
![](https://github.com/jasminehung/github-tutorial/blob/master/git.png)

* repository(repo) : 儲存庫，包含歷史紀錄的數據庫，可能含有多個branch
* clone : repo的副本copy，含有原repo中的各種訊息
* push : 將數據提交到遠端repo
* pull : 從遠端repo或本地branch取得數據並合併到指定分支
* branch : 分支，不同的開發路線
* merge : 將數據合併到分支
* commit : 將文件更改記錄到repo中

## Git指令 (git bash 中執行)
* git init : 在本地資料夾新增project (repo)
* touch: 新增檔案 (如: touch index.html)
* git add .  : 將目前全部檔案加入索引(待commit)
* git add (file名) : 將單一檔案加入索引(待commit)
* git status : 索引的狀態(若全部都commit出去了 status就是空的)
* git commit -m '...備註...': 提交commit
* mkdir : project中新增folder 如: mkdir css)
* git log : 查詢commit的紀錄
* 新增.gitignore檔 : 排除要被版控的檔案 [A collection of useful .gitignore templates](https://github.com/github/gitignore)
 * gitignore檔中寫入:
 * file_name.html (排除該html檔)
 *  .html (排除所有html檔)
 *  folder_name/ (排除整個folder)
 
HEAD : 目前所在的commit的位置的指標
* git reset HEAD file_name:檔案取消索引
* git reset HEAD : 全部檔案取消索引
* git checkout file_name : 還原單一檔案到上次commit的狀態
* git reset --hard : 還原工作目錄與索引到上次commit的狀態

![](https://github.com/jasminehung/github-tutorial/blob/master/branch.png)

* git branch : 列出所有分支，*號標住的是當前所在分支
* git checkout commit_id之前四碼 : 檢視以前commit版本
* git checkout master : 切換回最新的master commit
* git branch new_branch_name : 新增branch
* git checkout branch_name : Switch to該branch
* git merge branch_name : 合併兩分支，若有衝突會顯示merge conflict，需手動修改

標籤(如version1,version2...)
* git tag tag_name : 新增標籤
* git tag -am "備註" tag_name : 新增有備註的標籤
* git tag : 查詢標籤
* git tag 0n : 查詢詳細標籤
* git tag -d tag_name : 刪除標籤(不影響commit內容)
* git checkout tag_name : 切換到該tag的commit

stash: 暫存做到一半的東西，暫存紀錄可帶到其他branch中
* git stash : 暫存當前變更 (master中看不到暫存)
* git stash list : 查看所有stash紀錄 
* git stash pop : 還原暫存 
* git stash drop : 清除最新暫存
* git stash clear :  清除all暫存

## Github 指令
1. a. git clone http://...... : 從github抓到本機

  b. git pull : 存下github上最新的code (多人開發時最好每次都先pull，未pull就push可能產生衝突)
2. git add .
3. git commit
4. git push :更新到遠端資料庫(github)

* push master以外的branch到github會出現error
 * git remote : 查詢本地有多少遠端數據庫 (clone下來的遠端數據庫github預設叫做origin)
 * git push 遠端主機名稱(github是origin) branch_name : push新的branch到github

* git pull = git fetch+git merge : 有時不希望pull下來導致自己的數據庫太亂又擔心有衝突時，可先fetch(此時會多一個FETCH_HEAD的branch，等確定沒問題再merge FETCH_HEAD)
 * git fetch origin branch_name

## Github for Windows 
1. Clone in Desktop
2. Commit to master : 僅將記錄存放在本機的master branch中，尚未回存到遠端的github 上
3. Sync : 同步到雲端github
* fork : 等同於使用git clone複製他人專案到你的 GitHub 帳號下 (因你沒有權限編輯他人的專案)
### 多人開發時用
1. Clone in Desktop
2. Fork new branch
3. Publish
4. Sync
5. Create(Send) pull request
6. Repo擁有者會收到Pull requests, then Merge
## Github pages (host your webpages)
1. create new repo
2. Settings-Github pages
3. Source : choose master branch
## Reference
bitbucket : 可開免費private repo

[30 天精通 Git 版本控管](https://github.com/doggy8088/Learn-Git-in-30-days)

[github入門使用介紹](http://blog.kevinlinul.idv.tw/?p=369)

[常用 Git 命令清单](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)

[Git命令快速參考](https://backlogtool.com/git-guide/tw/reference/)
