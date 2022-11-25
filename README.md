# git-study
git命令学习 
# 基础命令

## 仓库

### 在当前目录新建一个Git代码库
git init

### 新建一个目录，将其初始化为Git代码库
git init [project-name]

### 下载一个项目
git clone [url]

## 配置

### 显示当前Git配置
git config --list

### 显示用户配置
git config --list --global

### 显示系统配置
git config --list --system

### 设置提交代码时的用户信息
git config [--global] user.name "[name]"
git config [--global] user.email "[email address]"

## 增加/删除文件
### 添加指定文件到暂存区
git add [file1] [file2] ...

### 添加指定目录到暂存区，包括子目录
git add [dir]

### 添加当前目录的所有文件到暂存区
git add .

### 删除工作区文件，并且将这次删除放入暂存区
git rm [file1] [file2] ...

### 停止追踪指定文件，但该文件会保留在工作区
git rm --cached [file]

### 改名文件，并且将这个改名放入暂存区
git mv [file-original] [file-renamed]

## 代码提交

### 提交暂存区到仓库区
git commit -m [message]

### 提交暂存区指定文件到仓库区
git commit [file1] [file2] ... -m [message]

### 省略‘git add’操作，直接提交到仓库区，只对修改和删除文件有效
git commit -a

### 使用一次新的commit，替代上一次提交
git commit --amend -m [message]

## 标签

### 列出所有tag
git tag

### 新建一个tag在当前commit
git tag [tag]

### 新建一个tag在指定commit
git tag [tag] [commit]

### 删除本地tag
git tag -d [tag]

### 删除远程tag
git push origin :refs/tags/[tagName]

### 查看tag信息
git show [tag]

### 提交指定tag
git push [remote] [tag]

### 提交所有tag
git push [remote] --tags

### 新建一个分支，指向某个tag
git checkout -b [branch] [tag]

## 查看信息

### 显示有变更的文件
git status

### 显示当前分支的版本历史
git log

### 显示commit历史，以及每次commit发生变更的文件
git log --stat

## 远程同步

### 下载远程仓库的所有变动 
git fetch [remote]

### 显示所有的远程仓库
git remote -v

### 显示某个远程仓库的信息
git remote show [remote]

### 增加一个新的远程仓库，并命名
git remote add [shortname] [url]

### 取回远程仓库的变化，并与本地分支合并
git pull [remote] [branch]

### 上传本地指定分支到远程仓库
git push [remote] [branch]

### 强行推送当前分支到远程仓库，即使有冲突
git push [remote] --force

### 推送所有分支到远程仓库
git push [remote] --all

## 撤销
### 恢复暂存区的指定文件到工作区
$ git checkout [file]

# 恢复某个commit的指定文件到暂存区和工作区
$ git checkout [commit] [file]

# 恢复暂存区的所有文件到工作区
$ git checkout .

# 重置暂存区的指定文件，与上一次commit保持一致，但工作区不变
$ git reset [file]

# 重置暂存区与工作区，与上一次commit保持一致
$ git reset --hard

# 重置当前分支的指针为指定commit，同时重置暂存区，但工作区不变
$ git reset [commit]

# 重置当前分支的HEAD为指定commit，同时重置暂存区和工作区，与指定commit一致
$ git reset --hard [commit]

# 重置当前HEAD为指定commit，但保持暂存区和工作区不变
$ git reset --keep [commit]

# 新建一个commit，用来撤销指定commit
# 后者的所有变化都将被前者抵消，并且应用到当前分支
$ git revert [commit]

暂时将未提交的变化移除，稍后再移入
$ git stash
$ git stash pop
