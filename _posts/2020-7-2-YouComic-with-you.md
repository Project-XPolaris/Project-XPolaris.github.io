---
title: YouComic 全家桶
tags: YouComic
comment: true
author: TakayamaAren
---

YouComic作为Project-XPolaris的一员，是针对文件服务器进行内容管理的一个套件，其下有多个工具可以提供相应的功能。YouComic主要围绕三个方面进行开发，专注于“标准化资源-管理资源-访问资源”这三个方向。<!--more-->

## YouComic Studio

[YouComic Studio](https://github.com/Project-XPolaris/YouComic-Studio)是关注于将资源标准化的工具。也是YouComic服务的入口。

主要支持的功能：

- 编辑书籍

对书页进行排版以及一些简单的编辑；同时也可以编辑书籍基本信息。完成后可以上传至YouComic服务中。

- 批量扫描书籍

扫描指定的文件夹，根据一定的规则识别出保存页面信息的文件夹，并匹配一些基本信息。扫描完成后，可以对扫描到的结果进行编辑，例如：设置封面、编辑标题、上标签，完成后可上传至YouComic。

- 编辑 MediaLobrary

Media Library是YouComic轻量的媒体库，相比于功能完整的YouComic服务来说，不需要依赖任何数据库等复杂的运行环境，数据保存在媒体库文件夹中，为其他YouComic提供索引服务。

使用YouComic Studio可以快速构建Media Library，编辑Media Library 中的书籍信息。


该软件基于Electron开发，所以你可以在大部分的平台使用，你可以在[Github Release](https://github.com/Project-XPolaris/YouComic-Studio/releases)页面中下载已编译的版本。

## YouComic Service

[YouComic Service](https://github.com/Project-XPolaris/YouComic-Server)是整个YouComic中最核心的服务组件，提供最基础的服务，包括管理书籍、页面文件管理等功能，并且其他套件一些功能也依赖此服务。应用封装了API接口与其他的套件进行交互。

支持最简单的一键部署，也支持docker部署；因此你可以在大部分的平台进行部署，例如：Windows、Linux等。当然也支持群晖（docker）、FreeNas等NAS文件管理系统上部署服务。

采用了Go语言编写，支持在大部分平台运行。你可以在[Github Release](https://github.com/Project-XPolaris/YouComic-Server/releases)页面中下载已编译的版本。

## YouComic-Nano

[YouComic-Nano](https://github.com/Project-XPolaris/YouComic-Nano)作为实现了YouComic Service 中最小的功能应用，仅支持最简单的浏览功能；结合Media Library，可以在网络上快速部署服务，大部分操作只需要一键，已经去除了一些不必要的功能配置。

## YouComic-Supervisor

作为服务的管理控制台，[YouComic-Supervisor](https://github.com/Project-XPolaris/YouComic-Supervisor)集成大量的YouComic核心服务的管理功能。包括书籍信息编辑、标签编辑、访问权限控制、用户编辑等管理功能

项目采用React编写，你可以在项目页面中下载至本地进行打包页面，并将其部署在Nginx、Apache等服务器软件上。

如果你不熟悉这些服务器软件，我们同时也提供相应的独立版本([YouComic-Supervisor-Standalone](https://github.com/Project-XPolaris/YouComic-Supervisor-Standalone))。该版本使用用Go语言编写了一个最简单的服务器程序。您可以[下载](https://github.com/Project-XPolaris/YouComic-Supervisor-Standalone/releases)相应系统的对应版本，直接可以使用。

## YouComic-Web

[YouComic-Web](https://github.com/Project-XPolaris/YouComic-Web),适配Web客户端，通过浏览器可以查看YouComic中的书籍信息。

## YouComic-Mobile-Suit

[YouComic—Mobile-Suit](https://github.com/Project-XPolaris/YouComic-Mobile-Suit)专门为移动设备打造的YouComic客户端，相较于网页版，移动版更加适配移动设备，在交互、流畅性、兼容性方面更加的适合移动设备

采用Flutter的跨平台的开发方式，用户可以在大部分的主流移动设备系统中使用移动版的客户端。你可以根据你的设备在[Github release](https://github.com/Project-XPolaris/YouComic-Mobile-Suit/releases/)页面来下载对应的应用安装包