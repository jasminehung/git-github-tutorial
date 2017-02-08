# github-tutorial
![](https://github.com/jasminehung/github-tutorial/blob/master/git.png)

* repository 仓库，包含文件历史记录和配置信息的数据库，通常含有多个分支；
* clone 仓库的克隆是指仓库的副本拷贝，一个新的克隆包含有原仓库的各种信息；
* push 将数据提交到远端仓库；
* pull 从远端仓库或本地分支获取数据，然后合并到指定分支；
* branch 不同的开发路线；
* merge 将数据合并到分支；
* commit 将文件更改记录到仓库中；

## Git指令
git bash 中執行
* git init : 在本地資料夾新增project (repo)
* touch: 新增檔案 (如: touch index.html)
* git add .  : 將目前全部檔案加入索引(待commit)
* git add (file名) : 將單一檔案加入索引(待commit)
* git status : 索引的狀態(若全部都commit出去了 status就是空的)
* git commit -m '...備註...': 提交commit
* mkdir : project中新增folder 如: mkdir css)
* git log : 查詢commit的紀錄
* touch .gitignore 排除要版控的檔案
 * gitignore檔中寫入:
 * file_name.html (排除該html檔)
 *  .html (排除所有html檔)
 *  folder_name/ (排除整個folder)
* git reset HEAD file_name:檔案取消索引
* git reset HEAD : 全部檔案取消索引
* git checkout file_name : 還原單一檔案到上次commit的狀態
* git reset --hard : 還原工作目錄與索引到上次commit的狀態

## github 指令
1. git clone http://...... : 從github抓到本機
2. git add .
3. git commit
4. git push :更新到遠端資料庫(github)

[A collection of useful .gitignore templates](https://github.com/github/gitignore)


## Github for Windows 

1.Clone in Desktop

* Commit to master : 僅將記錄存放在本機的master branch中，尚未回存到遠端的github 上
* Sync : 同步到雲端github

### 多人開發時用
1. Clone in Desktop
2. Fork new branch
3. Publish
4. Sync
5. Create(Send) pull request
6. Repo擁有者會收到Pull requests, then Merge

## Reference
bitbucket : 可開免費private repo

[github入門使用介紹](http://blog.kevinlinul.idv.tw/?p=369)
[常用 Git 命令清单](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)
[Git命令快速參考](https://backlogtool.com/git-guide/tw/reference/)
