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