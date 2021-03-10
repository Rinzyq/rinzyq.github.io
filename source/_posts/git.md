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

### 设置系统用户级别y邮箱

``` bash
$ git config -global user.email [email]
```

__作用：__ 设置系统用户级别邮箱

### 查看config文件内的签名以及邮箱

``` bash
$ cat .git/config
```
