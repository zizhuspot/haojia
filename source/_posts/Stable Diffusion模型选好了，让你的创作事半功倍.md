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

“选择合适的模型，随便出图，比打一堆提示词要好。”

事实上，高质量的模型，可以成倍地提高出图质量。目前，高质量的模型可以提高图片质量。 CivitAI（俗称 C 站， [https://civitai.com/](https://civitai.com/) ）是业内比较成熟的一个 Stable Diffusion 模型社区，上面收集了上千个模型，以及上万张附带提示词的图像，这大大降低了 Stable Diffusion 入门学习成本。

![](https://s2.loli.net/2023/07/27/X28Y5kEWjsAOnau.jpg)

下面简要介绍一下 C 站一些优秀的创作模型，并在文末结合示例进行应用说明。

## 一、C站模型分类

CivitAI 以上模型主要分为四类：Checkpoint、LoRA、Textual Inversion、Hypernetwork，分别对应 4 不同的训练方法。

- Checkpoint：通过 Dreambooth 训练方法得到的大模型， 特点是绘图效果好，但由于训练是一个完整的新模型，训练速度一般较慢，生成模型文件较大，一般有几个 G，文件格式为 safetensors 或 ckpt。

- LoRA：一种轻量化模型微调训练方法是在原有大模型的基础上，对模型进行微调，以输出具有固定特征的人或事。特点是具体风格特征绘图效果好，训练速度快，模型文件小，一般几十到一百多 MB，需要搭配大模型使用。

- Textual Inversion：一种使用文本提示来训练模型的方法可以简单地理解为一组包装提示，用于生成具有固定特征的人或事物。特点是特定风格特征的绘图效果好，模型文件很小，一般是几十个 K，但训练速度慢，需要搭配大模型使用。

- Hypernetwork：类似 LoRA，但是模型效果不如 LoRA，需要搭配大模型使用。

模型推荐：Checkpoint > LoRA > Textual Inversion > Hypernetwork

通常情况 Checkpoint 模型搭配 LoRA 或 Textual Inversion 使用模型，可以获得更好的绘图效果。

补充:还有一类 VAE 模型，简单理解它的作用是提高图像的色彩效果，使图像看起来不那么灰色，并对图像细节进行微妙的调整。

CivitAI 模型可以根据不同的分类和排序方法进行筛选和搜索。

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

## 总结

大家看到现在肯定已经知道模型的好处与重要性了，快来动手实践起来吧，Ai创作有很多的可能性与创意，认真学习AIGC相关的知识，就能更快更好的制作出更棒的艺术作品哦。

## Stable diffusion的实用关键词分享

1. 初始值：在解决实际问题时，需要对扩散过程的初始状态进行设定，即给出初值。

2. 时间步长：时间步长用于描述扩散过程中的每一步，控制着随机过程的快慢。

3. 空间步长：空间步长用于描述扩散过程中的每一步中，随机扩散粒子在空间中的移动距离。

4. 边界条件：边界条件用于限制粒子扩散的范围，常见的有周期边界、固定边界等。

5. 扩散系数：扩散系数用于描述粒子在单位时间内通过单位面积的扩散速率，是决定扩散过程的重要因素之一。

6. 源汇项：源汇项用于描述扩散过程中粒子源和粒子汇的分布情况，可以通过人为设定或根据实际问题计算得出。

7. 稳定化参数：稳定化参数用于控制随机过程的稳定性，防止扩散过程中出现数值不稳定的情况。

8. 高斯分布：高斯分布是一种常见的概率分布，用于描述随机过程中粒子的分布情况，也是Stable Diffusion中常用的分布函数之一。

9. 数值方法：数值方法是解决扩散方程的重要手段，如有限差分法、有限元法、谱方法等。

10. 并行计算：并行计算可以加速计算过程，提高计算效率，是处理大规模扩散问题时的必要手段之一。

以上是Stable Diffusion中常用的实用关键词，它们涵盖了Stable Diffusion的基本概念、计算方法、应用领域等方面。




