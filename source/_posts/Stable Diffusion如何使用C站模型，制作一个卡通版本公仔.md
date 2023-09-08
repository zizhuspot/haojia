---
title: Stable Diffusion如何使用C站模型，制作一个卡通版本公仔
date: 2023-07-27 18:24:49
categories:
  - Ai绘图
tags:
  - Stable Diffusion
  - Ai绘图
  - 创意艺术
  - 艺术创意
  - Ai工具
  
description: 本文介绍了使用Stable Diffusion下载C站模型，实战创作一个卡通公仔，对于AIGC整个创作流程更具体化

cover: https://s2.loli.net/2023/07/27/rezFAto3pB7VPCm.jpg

---

## Step 1: 模型下载与装载

**条件**：Stable Diffusion在本地已经部署成功。

**所需模型**：Checkpoint 模型（ReV Animated），Lora 模型（Blindbox）

- 下载 LoRA 模型： [https://civitai.com/models/25995/blindbox?modelVersionId=32988](https://civitai.com/models/25995/blindbox?modelVersionId=32988)（存放至本地 Lora 模型文件夹 /stable-diffusion-webui/models/Lora）

- 下载 Checkpoint 模型： [https://civitai.com/models/7371?modelVersionId=46846](https://civitai.com/models/7371?modelVersionId=46846)（放至本地 Checkpoint 模型文件夹 /stable-diffusion-webui/models/Stable-diffusion）

## Step 2:设置参数与提示词

除了手动输入提示词，设置参数外，还有一个比较简便的方式：直接从 CivitiAI 作品图中一键复制参数至 WebUI 中，再进行调整。

![](https://s2.loli.net/2023/07/27/py2MabrNl37KRSV.jpg)

![](https://s2.loli.net/2023/07/27/WXaoYDLrkqfedNO.jpg)

***提示词与参数设置：***

**Pompt**：(masterpiece), (best quality), (ultra-detailed), (full body:1.2), (simple background, white background:1.3), chibi, simple body, melting heart, purple leaves, purple hat, vivid color

**Negative Prompt**：(worst quality, low quality:1.4), lowres, bad anatomy, bad hands, text, error, missing fingers, extra digit, fewer digits, cropped, worst quality, low quality, normal quality, jpeg artifacts, signature, watermark, username, blurry

*Steps: 20, Sampler: DPM++ SDE Karras, CFG scale: 7.5, Size: 512x768*

## Step 3: 设置ControlNet，定制公仔专属形象

在这个实例中，我们要把一个平面卡通形象制作成一个 3D 公仔形象，因此需要通过[ControlNet](https://stablediffusionweb.com/ControlNet)的 lineart 和 depth 模型，构建公仔轮廓，再叠加盲盒模型定制出专属公仔形象。

![](https://s2.loli.net/2023/07/27/rezFAto3pB7VPCm.jpg)

## 总结：

通过这个制作卡通公仔的形象，相信大家对于如何使用模型已经有了一个基本的了解，最好自己动手试一试，才知道整个工作流程是如何实现的，最后祝大家学到更多的Ai艺术创作知识。

- *关于Ai绘图*

AI绘图可以应用于多个领域，包括但不限于：

1. 数据可视化：AI绘图可以帮助将大量的数据以图表的形式展示出来，使得数据更加直观和易于理解。例如，可以使用AI绘图来绘制折线图、柱状图、散点图等，以展示数据的趋势、分布等信息。

2. 图像生成：AI绘图可以生成各种类型的图像，包括自然景观、人物肖像、艺术作品等。通过训练模型，AI可以学习并模仿各种绘画风格，从而生成具有艺术性的图像。

3. 设计和创意：AI绘图可以用于设计和创意领域，例如绘制平面设计、插图、标志、海报等。AI可以根据用户的需求和输入的参数，生成符合要求的设计图案。

4. 辅助绘图工具：AI绘图可以作为辅助工具，帮助艺术家、设计师等快速生成草图、线稿等初步构思，从而提高创作效率。

总之，AI绘图可以在许多领域中发挥作用，帮助人们更好地表达和展示信息，提高创作效率和创意水平。

- *AI与设计可以合作吗？*

是的，人工智能可以用于设计。事实上，人工智能已经应用于各种设计领域，如创建徽标、生成网站布局，甚至设计时装。人工智能可以通过自动执行重复性任务、分析数据以识别模式和洞察力，以及产生新的设计理念来帮助设计师。例如，人工智能算法可以分析用户行为数据，帮助设计师创建更直观的用户界面。此外，人工智能还可以根据输入标准生成独特的设计，帮助设计师探索新的设计可能性。不过，需要注意的是，人工智能应被视为辅助设计师的工具，而不是人类创造力和直觉的替代品。

- *现在主流的Ai设计工具都有哪些呢？*

目前有几种主流的人工智能设计工具。下面是一些例子：

1. Canva - Canva 是一款流行的图形设计工具，它使用 AI 根据用户输入来建议设计元素和布局。

2. Adobe Sensei - Adobe Sensei 是一个人工智能平台，为设计师提供各种工具，如自动图像标记、内容感知填充和字体识别。

3. Sketch - Sketch 是一种流行的设计工具，它提供各种插件，利用人工智能自动执行重复性任务，协助设计师创建布局和设计。

4. Figma - Figma 是一款基于云的设计工具，它使用人工智能提供自动布局等功能，让设计师更轻松地创建响应式设计。

5. Autodesk Dreamcatcher - Autodesk Dreamcatcher 是一款生成式设计工具，它使用人工智能根据输入标准生成设计选项，让设计师探索更多设计可能性。

以上只是当今众多人工智能设计工具中的几个例子。随着人工智能的不断发展，我们有望看到更多的创新工具和功能，帮助设计师更高效、更有创意地工作。

## 如何提高自己使用Stable diffusion的使用水平?

- 要提高自己使用Stable Diffusion的使用水平，可以考虑以下几个方面：

- 熟悉Stable Diffusion的功能和使用方法：在开始使用Stable Diffusion之前，需要先了解它的功能和使用方法，包括如何设置参数、如何使用正则化方法缓解过拟合、如何扩容或剪枝模型以提高精度和训练速度等。

- 理解数据和模型：在使用Stable Diffusion时，需要清楚地了解所要研究的现象或问题，并将其转化为合适的数学形式。此外，需要设计合适的模型，并进行优化以提高模型的精度和泛化能力。

- 实践和探索：通过实践来不断提高自己的使用水平。可以尝试使用不同的模型和参数设置进行训练和预测，并分析结果，以了解不同参数和模型对结果的影响。同时可以探索使用Stable Diffusion的其他功能和应用，例如进行图生成等。

- 学习相关知识和技术：可以学习与Stable Diffusion相关的知识和技术，例如深度学习、概率图模型等，以更深入地了解Stable Diffusion的原理和应用。

- 参与社区和活动：可以参与Stable Diffusion的社区和活动，与其他使用者交流和分享经验，并获得帮助和支持。

总之，要提高自己使用Stable Diffusion的使用水平，需要不断学习和实践，并不断探索和拓展其应用领域。通过熟悉功能、理解数据和模型、实践和探索、学习相关知识和技术以及参与社区和活动等方式，可以逐步提高自己的使用水平。



