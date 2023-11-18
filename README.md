## 一、Git常用撤销操作

### 1、未git add 
直接使用`git checkout -- 文件`，即可撤销修改，撤销修改就回到和版本库一模一样的样子。

### 2、已 git add 未git commit
先使用`git reset HEAD -- 文件`，然后在使用`git checkout -- 文件`进行修改撤销。

### 3、已git commit未push
`git commit --amend`撤销最近一次提交

### 4、已push
`git reset --hard HEAD`回滚到最近的一次push版本
`git reset --hard <commit id>` 回滚到指定commit id的push版本

## 二、Git合并操作
### 1、git merge
git merge会将两个分支的修改合并成一个新的commit，保留两个分支的修改历史。执行git merge后分支图会呈现一个新的节点，表示合并后的结果。
### 2、git rebase
git rebase操作是将分支重放到另一个分支上，看上去就像该分支从该分支直线发散出来一样。执行git rebase后分支的历史会被整体前移，新的commit都会被放在目标分支上。
### 3、git squash
git squash会将多个commit squashed成一个commit。执行git squash后历史记录会被整合成一个新的commit，以简化历史。
