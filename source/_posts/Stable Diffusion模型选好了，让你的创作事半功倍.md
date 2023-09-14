---
title: Stable Diffusion模型选好了，让你的创作事半功倍
date: 2023-05-19 15:26:47
categories:
  - Ai绘图
tags:
  - Stable Diffusion
  - Stable Diffusion模型
  - Ai绘图
  - 艺术创作
  - Stable Diffusion实战
  - 创意艺术
  - Ai工具
  - 艺术创作
  - 人工智能
  - 艺术设计
description: Stable Diffusion模型选择与模型推荐，让你的工作效率与工作质量更高。

cover: https://s2.loli.net/2023/07/27/X28Y5kEWjsAOnau.jpg

---

"选择合适的模型，出图效果更佳，比繁琐的提示词来得轻松。"

事实上，一个高质量的模型能成倍提升出图质量。如今，优质模型已成为提升图片质量的关键因素。在众多Stable Diffusion模型社区中，CivitAI（又称C站，https://civitai.com/）已成为相对成熟的一个，提供了上千个优质模型以及上万张附带提示词的精良图像，从而降低了学习门槛。

以下是C站部分出类拔萃的创作模型的简介，并在文末进行了示例应用说明。

一、C站模型的分类

CivitAI的模型主要分为四种类型：Checkpoint、LoRA、Textual Inversion、Hypernetwork，分别对应着四种各具特色的训练方法。

Checkpoint：通过Dreambooth训练法锻造的大模型，它的绘图效果格外优异，但因为需要训练全新的模型，所以速度相对较慢，且生成的文件较大，通常可达几个G，文件格式为safetensors或ckpt。

LoRA：一种轻量化模型微调训练法，它以原有大模型为基础进行微调，以输出具有特定风格特征的人或事物。它的特点是在保持绘图效果的同时提高了训练速度，模型文件也相对较小，一般在几十到一百多MB，需要搭配大模型使用。

Textual Inversion：一种利用文本提示训练模型的方法，可以简单理解为一组调控提示，用于创生具有特定风格特征的人或事物。尽管它的训练速度较慢，但模型文件很小，一般是几十个K，需要搭配大模型使用。
Hypernetwork：与LoRA类似但效果略逊一筹的模型，需要搭配大模型使用。

推荐模型排名为：Checkpoint > LoRA > Textual Inversion > Hypernetwork

若想获得最佳的绘图效果，你可以将Checkpoint模型与LoRA或Textual Inversion模型搭配使用。

额外补充：还有一种VAE模型，它的作用在于提升图像的色彩效果，让图像看起来不再单调灰暗，同时对图像细节进行微妙的调整。

CivitAI的模型筛选与搜索功能强大，你可以根据不同的分类和排序方式筛选出最适合你的模型。

![](https://s2.loli.net/2023/07/27/NEsMOw2yz6YhTRp.jpg)

打开单个模型页面后，可以查看模型说明和下载模型。

![](https://s2.loli.net/2023/07/27/MslgPoxUcimZTWw.jpg)

## 二、模型推荐

### -Checkpoint模型

**-Lyriel-**

模型类别：Checkpoint 模型

下载地址： [https://civitai.com/models/22922/lyriel](https://civitai.com/models/22922/lyriel)

模型说明：胜任多种风格，能实现顶级的光影效果和人物风景细节。

参数推荐：DPM++2M Karras，Clip skip 2 Sampler，Step25-35+

![](https://s2.loli.net/2023/07/27/lL7ams3ogZeMQF2.jpg)

### -LoRA模型

**-blindbox-**

模型类别：LoRA 模型

下载地址： [https://civitai.com/models/25995/blindbox?modelVersionId=32988](https://civitai.com/models/25995/blindbox?modelVersionId=32988)

模型说明：可生成盲盒风格的模型，使用时主模型建议选 ReV Animated。

触发词：full body, chibi

![](https://s2.loli.net/2023/07/27/mT5V9NkJEZ1tnAl.jpg)

### -Tetual Inversion模型

模型存放路径：/stable-diffusion-webui/embeddings

**-SamDoesArts-**

模型类别：TEXTUAL INVERSION

下载地址： [https://civitai.com/models/1247/samdoesarts-embedding-1](https://civitai.com/models/1247/samdoesarts-embedding-1)

模型说明：SamDoesArt 画风。触发词：SamDoesArt1

![](https://s2.loli.net/2023/07/27/H5c4YCXSyTBUQ2d.jpg)

探索AI创作的无限可能性
看到了这里，相信大家已经深刻体会到AI模型的巨大优势和重要性了。赶快拾起你的创造之笔，融入AI的海洋，探索无穷无尽的创新之旅吧！只要努力学习并掌握AIGC的相关知识，你就能轻松制作出令人瞩目的艺术佳作。

下面，让我们来一起领略Stable Diffusion模型中的魔法关键词：

- 初始种子：想象一下，一切开始于一片混沌。在Stable Diffusion的世界中，我们需要设定扩散的初始状态，即为模型提供一些“种子”。

- 时间步伐：时间是生命的记录者，也是扩散过程的指挥者。每一个“时间步伐”代表着过程中的一小步，控制着随机过程的节奏。

- 空间步伐：空间，是扩散的舞台。每一个步骤中，随机扩散粒子在空间中的移动距离，就是空间步伐。

- 边界条件：边界就像城墙一样，限制了粒子的活动范围。有周期边界和固定边界等类型，为扩散过程划定界限。

- 扩散系数：想象一下，粒子在单位时间内通过单位面积的扩散速度就是扩散系数，它对扩散过程的快慢起着关键作用。

- 源汇项：源汇项就像是扩散过程中的粒子源和粒子汇，可以人为设定或根据实际问题计算得出，描述了粒子在扩散过程中的分布情况。

- 稳定化参数：小小参数，大大功能！稳定化参数可以有效控制随机过程的稳定性，让扩散过程更加稳定，防止数值不稳定的情况出现。

- 高斯分布：这个常见又神奇的分布，描述了随机过程中粒子的分布情况，也是Stable Diffusion中常用的分布函数之一。

- 数值方法：这些强大的计算手段，比如有限差分法、有限元法、谱方法等，是解决扩散方程的关键。

- 并行计算：当我们面对大规模的扩散问题时，并行计算就像魔法一样，它能加速计算过程，提高计算效率，成为我们必须掌握的利器！

以上就是Stable Diffusion中常用的关键词，它们带你走入这个模型的世界，帮你理解这个模型的基本概念、计算方法和应用领域。希望你在探索AI创作的旅程中，能充分享受这些关键词带来的启发和乐趣！




