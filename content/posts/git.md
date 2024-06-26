---
title : 'Git Logs - git学习备忘录'
date : 2024-06-28T00:01:04+08:00
draft : false
tags: ["git"]
categories: ["tech", "tutorial"]
---

## .gitignore 文件忽略内容
忽略MacOS下面的文件
*.DS_Store

匹配根目录下的 folder 文件夹
/folder/

取消对 folder 下的 a 文件夹的忽略
!/folder/a/

取消对 folder 下的 b 文件夹的忽略
!/folder/b/


## git commit 如何不添加注释
‘’‘
git commit -m "message"
’‘’
这个是必要的。如果铁了心不想添加注释
‘’‘ git commit --allow-empty-message -m "" ’‘’

## git pull 和 git fetch 区别

git fetch 命令是告诉你的本地 git 从源文件中检索最新元数据信息（但尚未进行任何文件传输，它更像是检查是否有可用的更新）。

git pull 会做相同的操作，还会从远程仓库中引入（复制）那些更新。

原文：[Git Fetch vs Pull: What's the Difference Between the Git Fetch and Git Pull Commands](https://www.freecodecamp.org/news/git-fetch-vs-pull/)