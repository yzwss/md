# Git
[Git 教程](http://www.runoob.com/git/git-tutorial.html)
## 安装
[msysGit](http://gitforwindows.org/)  
> git --version

## 配置
+ 系统级    /etc/gitconfig    git config --system
+ 用户级    ~/.gitconfig    git config --global
+ 项目级    .git/config    git config

设置变量
> git config --global user.name yangzhiwei  
> git config --global user.name zwyang@foxmail.com  

查看变量
> git config --list  
> vim ~/.gitconfig  
> git config user.name  

## 概念
+ 工作区  项目
+ 版本库(Git仓库) `.git` 是个目录，包含了暂存区文件，各分支文件及Git对象库
+ 暂存区(stage) `.git/index` 是个文件
+ Git对象库 `.git/objects` 是个目录
+ （分支-版本库中的文件/HEAD游标-指向某个分支-分支别名）

当对工作区修改的文件执行 `git add` 时，暂存区更新，同时工作区修改的文件内容被写入到对象库中的一个新的对象中，而该对象的ID被记录在暂存区。  
当执行提交操作`git commit`时，暂存区写到分支。  
当执行 `git reset HEAD` 命令时，分支写到暂存区，工作区不受影响。  
当执行 `git rm --cached <file>` 时，解除版本控制，直接从暂存区删除文件，工作区则不做出改变。  
当执行 `git checkout .` 或者 `git checkout -- <file>` 时，会用暂存区全部或指定的文件替换工作区的文件。这个操作很危险，会清除工作区中未添加到暂存区的改动。  
当执行 `git checkout HEAD .` 或者 `git checkout HEAD <file>` 时，会用分支中的全部或者部分文件替换暂存区和以及工作区中的文件。这个命令也是极具危险性的，因为不但会清除工作区中未提交的改动，也会清除暂存区中未提交的改动。  

## 创建版本库(创建仓库)
创建 `.git` 目录  
> git init  (当前目录下创建 `.git` 目录)  
> git init  specified-path  (某个指定的目录下创建 `.git` 目录)  

把文件纳入版本控制  
> git add *.c  
> git add README1 README2 README3  
> git add .
> git commit -m "初始化项目基线"  

复制版本控制的项目  
> git clone repo  (整个项目复制到当前目录下)  
> git clone repo specified-path  (项目中的内容复制到某个指定的目录下)  
> git clone git@github.com:yzwss/test.git  
> git clone git@github.com:yzwss/test.git test11  
> git clone https://github.com/yzwss/test.git  
> git clone https://github.com/yzwss/test.git test22  

## 基本操作（缓存区管理）
查看状态  
> git status -s  

查看改动  
git diff查看执行git status的结果的详细信息。  
git diff显示工作区与缓存区的区别。  
> git diff  尚未缓存的改动  
> git diff --cached  查看已缓存的改动  
> git diff HEAD  查看已缓存的与未缓存的所有改动  
> git diff --stat  显示摘要  

直接提交  
> git commit -a  
> git commit -am '提交文件'  

取消其中一个的缓存  
> git reset HEAD -- hello.php

删除文件  
如果只是简单地从工作目录中手工删除文件，运行 git status 时就会在 Changes not staged for commit 的提示仍然需要git add该文件才行。  
> git rm file 将本地删除和add合并成一步  
> git rm -f file 删除之前修改过，并且已经放到缓存区域  
> git rm --cached file 解除版本控制  
> git rm -r * 如果后面跟的是一个目录做为参数，则会递归删除整个目录中的所有子目录和文件。进入某个目录中，执行此语句，会删除该目录下的所有文件和子目录。  

移动文件  
> git mv file  

以上步骤都只是加入缓存区而已，还需要提交。  

## 分支管理
创建分支  
> git branch branchname

切换分支  
> git checkout branchname

创建切换分支  
> git checkout -b branchname

删除分支  
> git branch -d branchname

列出分支  
> git branch

合并分支  
> git merge branchname -m 'some desc'

合并时候产生冲突  
1. Automatic merge failed; fix conflicts and then commit the result.  
2. 手动修改文件  
3. 用Git add告诉Git冲突已经解决，然后做一次commit，完毕。如果没有冲突，相当于合并就自带了一次commit，不需要这次附加的commit  

# 查看历史
> git log  
> git log --oneline  
> git log --oneline --graph  
> git log --oneline --reverse  
> git log --author=Linus --oneline -5  
> git log --oneline --before={3.weeks.ago} --after={2010-04-18} --no-merges  

# 标签
> git tag v1.0  
> git tag -a v1.0 -m 'some desc'  -a 选项意为"创建一个带注解的标签"。  
> git log --oneline --decorate --graph  当我们执行 git log --decorate 时，我们可以看到我们的标签了  
> git tag v0.9 85fc7e7  给提交追加标签  
> git tag  查看所有标签  

# Github

