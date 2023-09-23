---
title: 有关Stable Diffusion插件的一切，看这一篇就够了！
date: 2023-05-16 18:19:25

categories:
  - Ai工具
tags:
  - Stable Diffusion
  - Ai绘图
  - Stable Diffusion模型
  - Stable Diffusion实战
  - 创意艺术
  - 艺术创意
  - Ai工具
  - 艺术创作
  - 人工智能
  - 艺术设计

description: 本文详细的介绍了安装/更新/卸载Stable Diffusion插件，让零基础的从业者也能从容不迫的进行工具更新与使用。

cover: https://s2.loli.net/2023/07/27/IRDMANqGWBtxHiv.png

---

![](https://s2.loli.net/2023/07/27/IRDMANqGWBtxHiv.png)

## 一、插件基础知识

Stable Diffusion WebUI，这款由大神Automatic1111精心打造的开源用户界面，紧紧围绕着Stable Diffusion模型，为的就是让咱们普通用户也能免费、轻松地体验到文生图技术的魅力！只要把它安装到本地，就能马上享受到这种科技盛宴。不得不提的是，自从WebUI横空出世，吸引了一大波AI绘画爱好者基于它开发出各种插件，不断优化拓展着WebUI的功能，简直是把咱们的体验推向了高潮！

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

如果你有幸使用由B站@秋葉 aaaki大佬亲自操刀的整合包，那么在启动WebUI之前，你只需点击启动器上的“**版本管理-拓展**”，就可以看到所有已经成功安装的插件更新状态。只要点击右上角的「**一键更新**」，一切就都搞定了！这个办法要比在WebUI里面进行更新快得多，省时又省力。而且你还可以在这里对插件进行卸载操作。偷偷告诉你，图中那两个显示“*非 Git 安装*”的插件，是因为它们是通过下载Zip压缩包的方式安装的，所以无法在这里直接更新。不过别担心，这并不影响你享受其他插件带来的便捷和乐趣！

![](https://s2.loli.net/2023/07/27/srEJNjObVR2opt4.jpg)

## 三、插件停用/卸载

### - 停用插件

打开 WebUI 界面，进入「*扩展-已安装*」，在列表内找到你想要停用的插件，取消它名称前面的勾选，然后点击「**应用并重启用户界面**」,重新进入后就看不到该插件了.这种方式会让插件不显示在 WebUI 的界面中，但是文件依旧会保存在根目录的「*Extensions*」文件夹中；恢复勾选并重启用户界面，就能再次看到这个插件 了.

![](https://s2.loli.net/2023/07/27/SCjx8uv2QNUlfDV.jpg)

### - 卸载插件

如果之后都不再使用某个插件，就可以打开根目录的「*Extensions*」文件夹，选中对应的插件文件夹，单击右键删除.然后重新启动 SD WebUI，插件就不存在了.如果你使用的是 B 站 @秋葉aaaki 大佬的整合包，也可以再启动器的“版本管理-拓展”中卸载对应的插件. 以上就是本次分享的Stable Diffusion WebUI插件的安装、更新、卸载方法。安装插件时，如果WebUI显示该插件已安装，则应在扩展中将其删除。首先，根目录中的一个文件夹。指定正确的文件并重新安装。

![](https://s2.loli.net/2023/07/27/QfpCkLsb2qOGH79.jpg)

### 关于stable diffusion,我的使用体验：

Stable Diffusion的ControlNet插件是一款强大到没朋友的工具，它的出现让Stable Diffusion这颗星辰的闪耀更加璀璨。这个插件的目的是提升算法的表现力，增加稳定性，赋予用户对算法的超精细控制权，满足形形色色的应用场景需求。下面，我将带你们探索我的使用体验哦！

安装和配置ControlNet插件就像是解谜游戏，一步一步慢慢来，一切都会水到渠成。首先，你需要下载并安装Stable Diffusion算法库，这就如同找到了一本魔法书。然后，你需要把ControlNet插件的源代码当做乐高积木，与算法库进行链接搭建。在配置的过程中，你需要揭开算法的神秘面纱，指定一些参数，例如时间步长、空间步长和扩散系数等。这些参数就像是魔法咒语，根据实际需要念咒调整，就可以激发出最佳的性能和稳定性。

完成了安装和配置，就像是获得了一把打开宝箱的钥匙，你可以开始畅玩ControlNet插件了！它支持多种应用场景，比如机器学习、自动控制等。在机器学习领域，ControlNet插件就像是一位神秘的法师，它可以与常见的机器学习框架如TensorFlow、PyTorch等结盟，一起施展稳定性和高效的训练魔法。

在自动控制领域，ControlNet插件就像是控制大师，它可以创作出精细的控制策略，随心所欲地控制系统行为。

在实际的应用中，我发现了ControlNet插件的几大优势：

它的稳定性简直逆天！ControlNet插件利用先进的稳定性理论来提升算法的稳定性，从而有效地降低了对计算资源的需求。
它性能爆棚！通过优化的算法和并行计算，ControlNet插件可以轻松处理大规模的数据集，而且计算速度飞快！
怎么样？是不是心动了？一起来体验这个强大的魔法世界吧！



