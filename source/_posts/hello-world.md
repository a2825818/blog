---
title: Hexo 安裝教學
date: 2018-04-11 10:12:03
tags:
- Hexo
- blog
---

## 介紹 Hexo

[Hexo](https://hexo.io/zh-tw/)是一款可自定義，輕量級，可部署在 Github 的部落格框架。


## 開始

### 下載 Nodejs

[node官網](https://nodejs.org/en/)

因為 Hexo 多半是用指令來安裝套件和執行，所以我們得下載 Nodejs

### 安裝 Hexo-cli

將 Hexo-cli 裝在全局，才可以使用 Hexo 下指令

``` bash
$ npm install -g hexo-cli

```


### hexo 創建一個部落格

它會自動生成一包資料夾，進到資料夾將套件安裝起來

``` bash
$ hexo init <folder>
$ cd <folder>
$ npm install
```



### 生成新文章

``` bash
$ hexo new "My New Post"
```


### 運行

``` bash
$ hexo server
```


### 生成靜態文件

``` bash
$ hexo generate
```


### 部署

``` bash
$ hexo deploy
```

