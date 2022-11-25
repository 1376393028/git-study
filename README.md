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
