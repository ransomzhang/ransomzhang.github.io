---
layout: wiki
title: Git
categories: wiki
description: Git cheatsheet
keywords: git, cheatsheet
---

### 配置
	$ git config --global user.name "Scott Chacon"
	$ git config --global user.email "schacon@gmail.com"

### clone 一个仓库
	git clone git://git.kernel.org/pub/scm/git/git.git

### 初始化一个仓库
	$ tar xzf project.tar.gz
	$ cd project
	$ git init

### 获取项目状况
	$ git status
	# On branch master
	# Changes to be committed:
	#   (use "git reset HEAD <file>..." to unstage)
	#
	#   modified:file1
	#   modified:file2
	#   modified:file3
	#

### 添加新内容到索引
	$ git add file1 file2 file3

### 查看哪些将被提交
	$ git diff --cached

### 提交 & 添加索引并提交所有
	$ git commit

	$ git commit -a

### 向代码仓库push代码
	$ git remote add <THEIR_REMOTE_URL>
	$ git push origin master
