- 新建分支：git checkout -b newDev 如果远程仓库有则从远程仓库拉取。没有则在本地新建分支 newDev
- 将本地新建的分支提交到远程仓库：git push origin newDev
- 切换分支：git checkout 'your 分支名'
- 合并分支：git merge newDev
- 删除本地分支：git branch -D newDev
- 删除远程分支：git push origin :newDev
- 将本地与远程关联起来： git push -u origin newDev,这样才能 push 和 pull
- 设置本地分支 test 与远程分支 dev 关联：git branch --set-upstream-to=origin/branch-name branch-name
  - 提交的时候 必须带上分支名：git push origin HEAF:dev 或者 git push origin test

### tag

- 创建 tag：git tag -a <tag-name> -m 'tag 描述' commit-id
- 查看 tag：git show <tag-name>
- 删除 本地 tag：git tag -d <tag-name>
- 推送本地 tag 到远程 origin ： git push origin <tag-name>
- 推送所有 tag 到远程分支 origin： git push origin --tags
- 删除远程 tag：git push origin :refs/tags/<tag-name>
-
