## Git常用撤销操作

### 1、未git add .
直接使用`git checkout -- 文件`，即可撤销修改，撤销修改就回到和版本库一模一样的样子。

### 2、已 git add .未git commit
先使用`git reset HEAD -- 文件`，然后在使用`git checkout -- 文件`进行修改撤销。

### 3、已git commit为push
`git commit --amend`撤销最近一次提交

### 4、已push
`git reset --hard HEAD`回滚到最近的一次push版本
`git reset --hard <commit id>` 回滚到指定commit id的push版本
