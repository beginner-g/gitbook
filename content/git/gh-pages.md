# gh-pages(分支)

### 分支操作(当前分支提交后创建新分支)

* 查看当前状态
  git status
* 创建新分支
  git branch [yourbranch](例：gh-pages)
* 查看分支
  git branch
* 创建并切换分支
  git checkout -b [yourbranch]
* 上传网上
  git push -u origin [yourbranch]
* 切换分支
  git checkout gh-pages

### 分支更新及合并(先切换主分支)

* 切换主分支
  git checkout master
* 合并其他分支代码
  git merge [otherbranch]
* git push
* 拉取主分支上的更新
  git pull origin master

### 删除分支

* 切换主分支
  git branch master
* 删除分支
  git branch -d [yourbranch]
