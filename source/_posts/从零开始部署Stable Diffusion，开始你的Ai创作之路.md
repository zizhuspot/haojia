---
title: 从零开始部署Stable Diffusion，开始你的Ai创作之路
date: 2023-05-21 08:20:32
categories:
  - Ai绘图
tags:
  - Stable Diffusion
  - 创意艺术
  - Ai绘图
  - 安装Stable Diffusion
  - Stable Diffusion模型
  - Stable Diffusion实战
  - Ai工具
  - 艺术创作
  - 人工智能
  - 艺术设计
  
description: 从零开始教授你如何部署Stable Diffusion，开始你的绘画创作之路，后面附赠汉化教程。

cover: https://s2.loli.net/2023/07/27/cn157qIGZH9wEOm.png

---

## 一、Step 1:部署Stable Diffusion之前

目前比较权威、可以在工作中使用的AI绘画软件只有两种。一种称为Midjourney（简称MJ），另一种称为[Stable Diffusion](https://stablediffusionweb.com/)（简称SD）。 MJ需要付费使用，而SD是开源免费的，但是入门难度和学习成本稍高，而且对于电脑配置（显卡、内存）来说非常昂贵。

SD和Midjourney相比，Stable Diffusion最大的优势是开源，这意味着Stable Diffusion潜力巨大，发展迅速。

![](https://s2.loli.net/2023/07/27/cn157qIGZH9wEOm.png)

由于开源、免费的属性，SD获得了大量的活跃用户，开发者社区为此提供了大量免费、高质量的外部预训练模型（[fine-tune](https://www.finetuneus.com/)）和插件目的，并不断维护和更新它们。在第三方插件和模型的支持下，SD比Midjourney拥有更丰富的个性化功能。经过用户调优后，可以生成更接近需求的图片。甚至在AI视频特效、AI音乐生成领域，Stable Diffusion也占据了一席之地。

稳定扩散是一种潜在扩散模型，能够从文本描述生成详细图像。它还可以用于图像修复、图像绘画、文本到图像和图像到图像等任务。简单来说，我们只需要给出所需图像的文字描述并提及稳定扩散即可生成符合您要求的逼真图像！

## 二、Step 2:电脑配置

电脑配置的核心要点：看显卡、看内存、看硬盘、看CPU。最重要的之一就是看显卡。 [Nvida英伟达](https://zh.wikipedia.org/zh-hans/%E8%8B%B1%E4%BC%9F%E8%BE%BE)独立显卡为首选，效率远高于集成显卡/AMD/Intel显卡和CPU渲染，最低10系列起步，体验更好用40系列，最低显存4G，6G合格，没有上限；内存最小8G，16G及格，无上限；硬盘可用空间最好有500G以上，固态最好。

系统要求：支持Win10/Win11/macOS（仅限Apple Silicon，Intel版Mac无法调用Radeon显卡）和Linux系统，Apple版SD兼容插件较少，功能不如Windows和Linux电脑。

![](https://s2.loli.net/2023/07/27/wprb4uiGfMKENZL.jpg)

从图中可以看出，Nvidia 的 GPU 提供了比 AMD 或英特尔的任何产品都优越的性能，有时甚至有很大优势。在 Torch 的 DLL 修复到位后，使用 xformers 时 RTX 4090 的性能比 RTX 3090 Ti 高 50%，不使用 xformers 时高 43%。生成每张图像只需要三秒多一点的时间。

## 三、Step 3:安装方法

SD开源地址：[https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki)
目前应用广泛的Stable Diffusion Web UI是一个发布在开源程序分享网站[Github](https://github.com/)上的Python项目。它与通常的软件安装方法不同。它不是一个下载安装后就可以立即使用的软件。需要准备不同操作系统的执行环境和编译源代码。

## 四、Step 4:启动Stable Diffusion

![](https://s2.loli.net/2023/07/27/dBG8qZtTrIFEHVx.jpg)

进入SD安装文件夹，双击**webui-user.bat**，加载后使用浏览器Chrome登录默认加载IP：*http://127.0.0.1:7860/*

## 五、Step 5:汉化Stable Diffusion

如果需要中文语言包，可以下载如下中文语言包扩展，下载界面网址为： [https://github.com/VinsonLaro/stable-diffusion-webui-chinese](https://github.com/VinsonLaro/stable-diffusion-webui-chinese)

***方法 ：通过 WebUI 拓展进行安装***

1.	打开 stable diffusion webui，进入"**Extensions**"选项卡

2.	点击"**Install from URL**"，注意"URL for extension's git repository"下方的输入框

3.	粘贴或输入本 Git 仓库地址 [https://github.com/VinsonLaro/stable-diffusion-webui-chinese](https://github.com/VinsonLaro/stable-diffusion-webui-chinese)

4.	点击下方的黄色按钮"**Install**"即可完成安装，然后重启 WebUI(点击"Install from URL"左方的"**Installed**"，然后点击黄色按钮"Apply and restart UI"网页下方的"**Reload UI**"完成重启)

5.	点击"**Settings**"，左侧点击"**User interface**"界面，在界面里最下方的"Localization (requires restart)"，选择"**Chinese-All**"或者"**Chinese-English**"

6.	点击界面最上方的黄色按钮"**Apply settings**"，再点击右侧的"**Reload UI**"即可完成汉化


