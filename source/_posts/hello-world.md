---
title: Hexo 安裝教學
date: 2018-04-14 10:12:03
tags:
- Hexo
- blog
---

## 介紹 Hexo

[Hexo](https://hexo.io/zh-tw/)是一款可自定義，輕量級，可部署在 Github 的部落格框架。


## 開始

> 環境需求
> - Git
> - Nodejs

### 下載 Nodejs 和 Git

[Git官網](https://git-scm.com/)
[Node官網](https://nodejs.org/en/)

我們安裝 Node 後，就能使用 NPM 來管理我們的工具包，因為 Hexo 多半是用指令來安裝套件、執行和部署。

### 安裝 Hexo-cli

將 Hexo-cli 裝在全局，才可以使用 Hexo 下指令

```code
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

新增一篇新文章，預設會在 _posts 下面

``` bash
$ hexo new "My New Post"
```

或是新增一個分類，它會自動在幫你新增此分類下的第一篇文章

``` bash
$ hexo new page "about"
```

### 清除已生成靜態文件

``` bash
$ hexo clean
```


### 生成靜態文件

如果有頁面結構有修正，需要清除後重新生成，才看得到改變。

``` bash
$ hexo generate
```


### 運行

可以運行在 http://localhost:4000 上看一下結果。

``` bash
$ hexo server
```


### 部署

先在 _config.yml 先設定好要 push 的地方位置，在這裡也要設定一下SSH，等等才能順利傳上去。

``` bash
deploy:
  type: git
  repo: git@github.com:yourname/yourname.github.io.git
  branch: master
```

安裝 hexo-deployer-git 套件，才能夠用指令的方式部署到 Github。

``` bash
$ npm install hexo-deployer-git --save

```

下了指令·就會按照所設定的，自動部署。
就可以在自己的 yourname.github.io 上看到自己的部落格。

``` bash
$ hexo deploy
```


### 更換版型

先到 [hexo](https://hexo.io/themes/) 挑一個自己喜歡的版型，然後將它 pull 下來到 themes 資料夾內。

```
git clone https://github.com/imbyron/hexo-theme-icalm.git ./themes/icalm
```


然後在 _config.yml 設定

```
theme: icalm
```

每個版型可能有不同的配置，大概參考一下作者的文件修改。

如果有自己想要換圖或改CSS的地方，只要進到版型的 source 裡去修改即可。

