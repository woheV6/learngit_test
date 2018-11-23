# git 学习笔记

### 初始化 git 仓库

- git init
- 将文件添加的版本库 git add <file>
- git commit -m '蛛丝马迹'
- pull
- push

### 生成 SSH

- ssh-keygen -t rsa -C "youremail@example.com" (一路回车就可以了)

- 主目录里找到.ssh 目录，里面有 id_rsa 和 id_rsa.pub 两个文件，这两个就是 SSH Key 的秘钥对，id_rsa 是私钥，不能泄露出去，id_rsa.pub 是公钥
- 2 步：登陆 GitHub，打开“Account settings”，“SSH Keys”页面：然后，点“Add SSH Key”，填上任意 Title，在 Key 文本框里粘贴 id_rsa.pub 文件的内容：

### 关联 仓库

- git remote add origin 你的仓库地址
- 本地库的所有内容推送到远程库上：git push -u origin master

### 克隆远程仓库

- git clone 你的远程仓库地址

### 分支

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

### gitignore 忽略文件)

- 在根目录创建 .gitignore 文件.
- 如果该文件在 .gitignore 文件中了，你想强制加到版本库中，git add -f <file-name>
