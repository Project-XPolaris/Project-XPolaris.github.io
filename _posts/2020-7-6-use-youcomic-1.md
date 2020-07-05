---
title: YouComic 使用 部署
tags: YouComic
comment: true
author: TakayamaAren
---

初见YouComic的用户，应该会对YouComic项目中众多的组件所迷惑，可能还会产生使用会很繁琐的错觉。其实不然，开发者一直都在朝着自动化的方向在开，并且会根据不同的使用环境来适配YouComic服务，这些服务可大可小，目的就是方便在不同的环境中使用。
<!--more-->
## 概述
在实际使用中只需要最简单的部署一个服务(目前为[YouComic Service](https://github.com/Project-XPolaris/YouComic-Server)或[YouComic-Nano](https://github.com/Project-XPolaris/YouComic-Nano))

这两个核心服务提供了最基础的服务，即内容管理的基础功能，在此基础上加上了HTTP的API接口组成。除此之外的组件都是使用这些服务的应用软件，使用者可以根据实际情况选择性的使用。

## 核心服务

### YouComic Service

作为核心服务，最简单的方式就是下载你已编译好的文件，直接点击运行。再使用之前不需要特别的繁琐的配置。首次启动会在在浏览器中配置相关选项。

![](/assets/images/article/2/p1.png)
当然大部分的选项都是不需要更改，如果不知道某一项具体的作用，可以保持使用默认值。

### YouComic Nano

这是最小的服务，仅保留了最简单的书籍和标签功能，主要为了提供给一下不便于部署复杂环境的场合，也不具备管理功能，仅保留浏览功能。

只需要一个可执行文件，初次会使用YouComic的扫描引擎对整个目录结构进行扫描，用户可以在YouComic Studio中编辑。