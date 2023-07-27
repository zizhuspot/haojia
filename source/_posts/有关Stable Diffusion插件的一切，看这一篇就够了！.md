---
title: 有关Stable Diffusion插件的一切，看这一篇就够了！
date: 2023-05-16 18:19:25

categories:
  - Stable Diffuse插件
tags:
  - Stable Diffuse插件
  - Stable Diffuse
  - Stable Diffuse安装
  - Ai作图

description: 本文详细的介绍了安装/更新/卸载Stable Diffusion插件，让零基础的从业者也能从容不迫的进行工具更新与使用。

cover: https://s2.loli.net/2023/07/27/IRDMANqGWBtxHiv.png

---
# 有关Stable Diffusion插件的一切，看这一篇就够了！

![](https://s2.loli.net/2023/07/27/IRDMANqGWBtxHiv.png)

## 一、插件基础知识

Stable Diffusion WebUI 是大神 Automatic1111 围绕 Stable Diffusion 模型开发的一款开源用户界面，可以安装到本地，让我们普通用户也可以免费、便捷地体验文生图技术. WebUI 出现后，又有很多 AI 绘画爱好者基于它开发出各种插件，用来优化拓展 WebUI 的功能。

爆红的插件 Controlnet 就是其中之一.这些插件都是免费开源的，它们的程序及代码一般会托管在 [Github](https://github.com/) 平台上，供公众免费取用，这也是为什么我们下载 WebUI 插件都绕不开 Github。

![](https://s2.loli.net/2023/07/27/d6gXeJBoSq4D8vy.jpg)

知名插件 Controlnet 的 Github 主页，[https://github.com/Mikubill/sd-webui-controlnet](https://github.com/Mikubill/sd-webui-controlnet)。

在 Github 上我们可以看到插件的详细信息，包括插件概述、功能介绍、安装/使用方式、安装需求、注意事项等，插件安装下载用到的也都是这里的资源，大家在安装一款插件之前，应该仔细阅读 Github 页面的内容. 

![](https://s2.loli.net/2023/07/27/oP3IlvZkY4c8NB2.jpg)

插件安装后，会自动显示在 WebUI 的操作界面中.在 「**扩展-已安装**」中可以查看所有安装成功的插件，并进行更新操作；插件对应的源文件都保存在 SD WebUI 根目录的 「*Extensions*」文件夹中，这个文件夹也是我们管理插件的重要途径之一。

![](https://s2.loli.net/2023/07/27/qPWRTOmY1diN7AS.jpg)

![](https://s2.loli.net/2023/07/27/tgKHF6kDclwdPmL.jpg)

*以Prompt All-in-One插件为例，一一介绍安装方法，按照 Github 页面之一上的介绍进行操作。*

- 提示多合一插件接口：[https://github.com/physton/sd-webui-prompt-all-in-one](https://github.com/physton/sd-webui-prompt-all-in-one)

- 提示一体式插件安装概述：文档 ([physton.github.io](https://physton.github.io/sd-webui-prompt-all-in-one-assets/#/zh-cn/Installation))

## 二、插件更新

插件更新的方式有 2 种，一是打开 SD WebUI，进入「*扩展-已安装*」，点击「**检查更新**」按钮，等待进度完成，然后点击「**应用并重启用户界面**」，插件更新就完成了。

![](https://s2.loli.net/2023/07/27/XJPv5SZtNnL1z8q.jpg)

如果你使用的是 B 站 @秋葉 aaaki 大佬的整合包，那么可以在启动 WebUI 之前，点击启动器的“**版本管理-拓展**”，在里面可以看到所有成功插件的更新状态，点击右上角的「**一键更新**」即可，这比在 WebUI 中更新要快很多，还可以对插件进行卸载. 可以看到下图中有两个插件显示“*非 Git 安装*”，这是因为它们是用下载 Zip 压缩包的方式安装的，所以无法在这里直接更新. 

![](https://s2.loli.net/2023/07/27/srEJNjObVR2opt4.jpg)

## 三、插件停用/卸载

### - 停用插件

打开 WebUI 界面，进入「*扩展-已安装*」，在列表内找到你想要停用的插件，取消它名称前面的勾选，然后点击「**应用并重启用户界面**」,重新进入后就看不到该插件了.这种方式会让插件不显示在 WebUI 的界面中，但是文件依旧会保存在根目录的「*Extensions*」文件夹中；恢复勾选并重启用户界面，就能再次看到这个插件 了.

![](https://s2.loli.net/2023/07/27/SCjx8uv2QNUlfDV.jpg)

### - 卸载插件

如果之后都不再使用某个插件，就可以打开根目录的「*Extensions*」文件夹，选中对应的插件文件夹，单击右键删除.然后重新启动 SD WebUI，插件就不存在了.如果你使用的是 B 站 @秋葉aaaki 大佬的整合包，也可以再启动器的“版本管理-拓展”中卸载对应的插件. 以上就是本次分享的Stable Diffusion WebUI插件的安装、更新、卸载方法。安装插件时，如果WebUI显示该插件已安装，则应在扩展中将其删除。首先，根目录中的一个文件夹。指定正确的文件并重新安装。

![](https://s2.loli.net/2023/07/27/QfpCkLsb2qOGH79.jpg)

