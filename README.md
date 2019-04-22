#git学习笔记:
git reset --hard HEAD^ 重置到上一个提交
git reset --hard xxx   重置到某个提交
git checkout -- readme.txt  放弃工作区的修改 放弃文件的修改
git reset HEAD <file> 	取消加入暂缓区
查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

git merge --no-ff -m "merge with no-ff" dev

git stash

git stash list

git stash apply

git stash pop

git branch -D <name>强行删除。

$ git branch --set-upstream-to=origin/dev dev

git reset --hard <commit_id> 

git push origin HEAD --force  //固定模式，不需要改变单词

回到某个版本
git revert -n 版本号”反做，并使用“git commit -m 版本名”提交：

git reset --hard 目标版本号”命令将版本回退：

git rebase --onto master server client
“取出 client 分支，找出 client 分支和 server 分支的共同祖先之后的变化，然后把它们在 master 上重演一遍”

git rebase master server  ebase [主分支] [特性分支] 命令会先取出特性分支 server，然后在主分支 master 上重演：

git rebase [startpoint] [endpoint] --onto [branchName]
