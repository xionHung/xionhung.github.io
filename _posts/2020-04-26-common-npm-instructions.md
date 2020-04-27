---
layout: post
title:  "npm的一些基本常用指令"
categories: npm
tags:  npm 
author: xionhong
---

* content
{:toc}

## 前言

> 收集一些常用的npm指令

## NPM

### 查看 npm 的版本

    npm -v

### 安装包

    npm install xxx  
    # 也可以写成
    npm i xxx
    # i 为 install 简写，下面出现的i 也都是install

    npm i xxx --save
    # --save 表示安装生产依赖包，会在 package.json/dependencies 下记录安装的包版本信息
    # 简写
    # npm i xxx -S 

    npm i xxx --save-dev
    # --save-dev 表示安装开发依赖包，会在package.json/devDependencies 下记录安装的包版本信息
    # 简写
    # npm i xxx -D






> 关于生产依赖和开发依赖，我这边也简单叙述一下  
> 
> - 生产依赖：就比如你使用`vue`开发，项目上线了，但是还是需要用到vue的语法去支持吧？  
> 
> - 开发依赖：就好比如`eslint`，这个模块是用来检查你开发代码规不规范，上线了，就用不到它了
> 
> 希望我的这些浅显的举例能帮助你更好的理解

### 初始化

    npm init
    # 输入一些关于本项目的一些基本信息，文件夹生成package.json文件，则初始化完成

### 卸载安装包

    npm uninstall xxx 或  npm remove xxx

### 查看安装包的详细信息

    npm info xxx

### 查看安装包的所有版本号

    npm view xxx versions

### 查看安装包的最新版本

    npm view xxx version

### 查看安装包的当前版本

    npm ls xxx

### 安装指定版本的包

    npm i xxx@0.0.1
    # 0.0.1 指要安装的版本号

### 查看项目安装了哪些包

    npm list

### 查看全局安装包的存放位置

    npm root -g

### 修复安装包

    npm audit fix

### 修改npm的下载镜像为淘宝镜像

    npm config set registry https://registry.npm.taobao.org

### npm缓存腐败

    npm cache clean --force

> - **问题情景：**可能是你删除node_modules，或者重新clone代码后，npm i的时候报错
> - **解决：**执行`npm cache clean --force`，如果执行后，npm i 还是报错的话，就删除package-lock.json再重新尝试一下~

## 总结

> 以上就是我收集且比较常用到的npm指令，作为记录，也希望能帮助到你~