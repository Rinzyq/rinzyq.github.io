---
title: git常用命令
date: 2021-03-10 20:25:38
tags:
---
这是一篇自学记录git命令行工具的常用命令总结，可能会有一些错误。

## 本地库初始化

``` bash
$ git init
```

__作用：__ 初始化本地库

## 设置签名

### 设置项目级别签名

``` bash
$ git config user.name [name]
```

__作用：__ 设置项目级别签名

### 设置项目级别邮箱

``` bash
$ git config user.email [email]
```

__作用：__ 设置项目级别邮箱

### 设置系统用户级别签名

``` bash
$ git config -global user.name [name]
```

__作用：__ 设置系统用户级别签名

### 设置系统用户级别邮箱

``` bash
$ git config -global user.email [email]
```

__作用：__ 设置系统用户级别邮箱

### 查看config文件的签名及邮箱

``` bash
$ cat .git/config
```

## 本地库的一些操作

### 查看本地库状态

``` bash
$ git status
```

__作用：__ 查看本地库的当前状态

### 暂存区的添加操作

``` bash
$ git add [file]
```

__作用：__ 将文件添加至暂存区

### 暂存区的撤回操作

``` bash
$ git rm --cached [file]
```

__作用：__ 将暂存区的文件撤回

### 本地库的提交操作

``` bash
$ git commit [file] 
```

__作用：__ 将文件提交到本地库

``` bash
$ git commit -m "message" [file] 
```

__作用：__ 将文件提交到本地库,并且在双引号内直接编辑message

## git的版本信息

``` bash
$ git log
```

__作用：__ 查看历史版本信息

``` bash
$ git log --oneline
```

__作用：__ 以一行显示历史版本信息，只显示当前版本到过去的版本

``` bash
$ git reflog
```

__作用：__ 简略显示历史版本信息，显示HEAD指针从当前版本移动到目标版本所需要的步数，并且显示所有版本

## 版本的前进后退

``` bash
$ git reset --hard [局部索引值] 
```

__作用：__ 跳转到索引值对应的版本

``` bash
$ git reset --hard HEAD^
```

__作用：__ 跳转到上一版本

``` bash
$ git reset --hard HEAD~[n]
```

__作用：__ 跳转到第N步的版本

```bash
--hard  //在本地库移动HEAD指针，重置暂存区和工作区
--mixed //在本地库移动HEAD指针，重置暂存区
--soft  //仅在本地库移动HEAD指针
```

## 比较文件

``` bash
$ git diff [file]
```

__作用：__ 比较文件修改前后差异，是与暂存区进行比较

``` bash
$ git diff HEAD [file]
```

__作用：__ 比较文件修改前后差异，是与本地库的文件进行比较

## 分支操作

``` bash
$ git branch -v
```

__作用：__ 查看现有分支

``` bash
$ git branch [分支名称]
```

__作用：__ 创建一个新的分支

``` bash
$ git checkout [分支名称]
```

__作用：__ 切换分支

``` bash
$ git merge [分支名称]
```

__作用：__ 将输入的分支名称合并到当前分支

## 与远程库的一些操作

### 赋值地址

``` bash
$ git remote add [自定义名称] [地址]
```

__作用：__ 将远程地址赋值到自定义名称

``` bash
$ git remote -v 
```

__作用：__ 显示所有定义的远程地址

### push操作

``` bash
$ git push [地址] [分支名称]
```

__作用：__ 将分支push到远程库

### clone操作

``` bash
$ git clone [地址]
```

__作用：__ 将该地址下的远程库克隆到当前项目

### fetch操作

``` bash
$ git fetch [地址] [分支名称]
```

__作用：__ 抓取远程地址上的远程库

### pull操作

``` bash
$ git pull [地址] [分支名称]
```

__作用：__ 直接拉去远程低智商的远程库覆盖本地库