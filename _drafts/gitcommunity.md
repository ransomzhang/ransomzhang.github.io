---
layout: post
title: Git Community book 笔记
categories: [玩物, 笔记]
description: git学习笔记 
keywords: git 
---

### 安装

	$ apt-get install git-core   #ubuntu
	$ yum install git-core    #centos

### 初始化

	$ git config --global user.name "ransom zhang"
	$ git config --global user.email "zhangransom@gmail.com"

之后主目录下会看到，全局设置

	ransom@rszpc:~$ cat ~/.gitconfig 
	[user]
		name = ransom zhang
		email = zhangransom@gmail.com

# 基本用法

### clone一个仓库

	git clone git://git.kernel.org/pub/scm/git/git.git      #git协议
	git clone http://www.kernel.org/pub/scm/git/git.git   #http协议

### 初始化一个仓库

	$ tar xzf project.tar.gz
	$ cd project
	$ git init

之后git会输出

	ransom@rszpc:~/Workspace/readingnotes$ git init
	Initialized empty Git repository in /home/ransom/Workspace/readingnotes/.git/
	ransom@rszpc:~/Workspace/readingnotes$ cd .git/
	ransom@rszpc:~/Workspace/readingnotes/.git$ ls
	branches  config  description  HEAD  hooks  info  objects  refs
