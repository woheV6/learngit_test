- 新建分支：git checkout -b newDev 如果远程仓库有则从远程仓库拉取。没有则在本地新建分支newDev
- 将本地分支提交到远程仓库：git push origin :newDev
- 合并分支：git merge newDev
- 删除分支：git checkout -d newDev

