---
title: hexo搭建博客(4)——跨电脑写博客策略
date: 2017-07-04 10:58:43
tags: [git]
categories: hexo
---
> 很多人搭建了hexo后发现，换了电脑根本没环境再写博客，难道要重搭环境？其实不，在hexo中其实有一个.gitignore文件，从文件夹就可以理解开发环境应该也要给放到github上。当然，这是其中一个途径，其他途径等着读者发现了。

## 创建多分支
个人感觉git的精髓除了分布式版本管理之外，就是分支的概念了。我们可以在静态网站的远程仓库上分别建两个分子，master分支是必须的，我们用master分支来存储hexo生成出来的静态文件。之后再创建一个hexo(名字你们可以自己另起)分支，用来存放hexo init 的源码。这样我们一个仓库就能通过切换不同分支来完成博客的生成和发布了。

> 相关命令
> 1. 仓库分支并切换分支
> git checkout -b hexo 
>>  1.1 clone后检出远程分支  
>>  git checkout -b hexo origin/hexo
> 
> 2. 推送分支到远程仓库
> git push origin hexo
> 
> 
> 4. 安装hexo(主要,机器必须有node.js环境)
> npm install hexo-cli -g
> 
> 5. 保存安装设置
> npm install --save