---
title: "Git"
date: 2021-08-03T17:08:33+08:00
lastmod: 2021-08-03T17:08:33+08:00
draft: false
keywords: []
description: ""
tags: [Pro Git]
categories: [Git]

reward: false
mathjax: false
mathjaxEnableSingleDollar: false
mathjaxEnableAutoNumber: false
enableOutdatedInfoWarning: true
---

## 起步
### vertion contral system发展的历史
从最开始的本地版本控制（存储在本地硬盘）到后来的集中式版本控制（有一个集中的存储服务器）再到后来的分布式版本控制（有多个存储服务器）
### Git为什么是Git
1. 记录的是文件快照，而不是记录差异，数据像是快照流
2. Git存储所有的历史记录，而不只是一个文件快照，你可以在本地完成几乎所有操作，而且不用担心历史记录的丢失
3. SHA-1计算校验和对数据进行引用，保证数据的完整性
4. 一般只添加数据，很难丢失数据
### Git的三种状态
三种状态对应于三种工作区域
* Working Directory: 你从.git directory拉取出来的某一个版本的文件区域，平时xx修改文件的地方（已修改）
* Staging Area: .git 中的一个文件保存你下次要提交的文件列表信息（暂存）
* .git directory: 保存项目元数据及对象数据库的地方(已提交)
### git config
* system : git config --system , /etc/gitconfig
* global : git config --global , ~/.gitconfig OR ~/.config/git/config
* local  : git config , ./.git/config
初次配置：
``` bash
git config --global user.name "Song Tianxiang"
git config --global user.email Songtx29.gmail
git config --global core.editor nvim
```
检查配置:
git config --list
git config <key>
### git help
``` bash
git help <verb>
git <verb> --help
man git-<verb>
```
