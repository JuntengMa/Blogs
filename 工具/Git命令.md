---
title: "自己比较常用的一些git操作"
categories: tools
tags: Git
top: 88 #是否置顶
cover: https://drscdn.500px.org/photo/266684907/q%3D80_h%3D450/v2?sig=fddd93a565bfc0a0a823bc71cd0423438214b85fcf84920f0a505614f87b5e75
coverWidth: 1200
coverHeight: 750
height: 750
---
# GIT 常用命令
<!--more-->

## 01 - 初始配置

```
- git init 初始化本地git仓库（创建新仓库）

- git config --global user.name "xxx" 配置用户名

- git config --global user.email "xxx@xxx.com" 配置用户邮箱

- git clone "git链接" 克隆git仓库到本地

- git status 查看当前在哪个分支
```

## 02 - 开发完毕将要上传代码仓库操作

```
git add .  增加当前子目录下所有更改过的文件至index

git commit -m "xxx" 提交

git push 推送改动到远端
```

## 03 - 新建分支操作

```
git branch <分支名> 创建新分支

git checkout <分支名> 切换到该分支

git push 如果是新建分支，push的时候需要跟远端仓库关联，一般会提示 git push --set-upstream 你的分支名 ， 复制提示信息并执行
```

## 04 - 合并分支操作

```
git pull origin master 多人协作，以防master已更新，本地代码版本没有更新，先同步一下master代码，以防产生合并冲突

git checkout master 先切换到主分支再合并

git merge <需要合并到master上的分支名> 合并某一个分支到该分支
```

## 05 - 删除本地，远程分支

```
- git branch -d <分支名> 删除本地某一分支

- git push origin --delete <分支名> 删除远端分支
```

## 06 - 版本回退

```
- git log 查看提交历史和commit 标记

- git reset --hard <commit 后面的字符串> 将代码回退到某一版本

- git push -f 远端仓库版本高于本地版本，需要强制推送上去
```

## 07 - 取消所有本地修改

```
git checkout .
```

## 09 - 查看修改

```
git show <commit日志>  显示详细更改
```

## 10 - 查看某一文件所有修改历史

```
 git log --pretty=on 相对路径/绝对路径

 git show <commit日志>
```

## 11 - 其他命令

```
git pull 从当前分支远端拉取代码

git pull origin <分支名> 拉取某一分支的代码并合并到当前分支

git branch 显示远程仓库分支

git branch -a 显示所有分支

git branch --merged 显示所有已合并到当前分支的分支

git branch --no-merged 显示所有未合并到当前分支的分支

git push origin master 推送到主分支

git pull origin <分支名> 拉取远程分支合并到当前分支

git log 显示提交日志

git diff 显示所有变更

git diff HEAD^ 显示与上个版本的差异

git rm xxx 除某文件
```

