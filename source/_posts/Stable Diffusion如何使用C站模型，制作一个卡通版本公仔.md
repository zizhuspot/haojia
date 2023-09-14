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
  
description: 这篇文章将带您领略如何使用Stable Diffusion来下载C站的模型，并通过实际创作一个可爱的卡通公仔来将AIGC的整个创作流程具体化。

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

通过亲手制作一个可爱的卡通公仔，相信大家已经对如何使用模型有了一个直观的了解。只有亲自动手尝试，才能真正掌握整个工作流程是如何实现的。希望大家都能从中学习到更多有关AI艺术创作的知识！

下面来聊一聊AI绘图的一些应用领域吧！
数据可视化：AI绘图能够轻松将大量数据以图表形式呈现出来，使得数据更加一目了然，便于理解。例如，我们可以使用AI绘图来生成折线图、柱状图、散点图等，帮助我们更好地了解数据的趋势、分布等信息。

AI绘图还能生成各种类型的图像，包括自然景观、人物肖像、艺术作品等。通过训练模型，AI可以学习和模仿各种绘画风格，从而生成极富艺术性的精美图像哦！

此外，AI绘图在设计和创意领域也大放异彩。它可以用于绘制平面设计、插图、标志、海报等，根据用户的需求和输入参数，生成符合要求的设计图案，为你的创作事业添砖加瓦！

最后，AI绘图还是一款强大的辅助绘图工具。它可以帮助艺术家、设计师等快速生成草图、线稿等初步构思，从而提高创作效率。总之，AI绘图在许多领域都能发挥它的神奇作用，帮助人们更好地表达和展示信息，提高创作效率和创意水平！

- *AI与设计可以合作吗？*

没错，人工智能确实可以用于设计，而且它的应用已经遍布各个领域。想象一下，从徽标到网页布局，再到时尚设计，人工智能的潜力真是无穷无尽！它像一个不知疲倦的助手，自动执行重复性任务，帮助设计师轻松地分析数据，找出隐藏在其中的模式和洞察力。

不仅如此，人工智能还能为设计师带来全新的设计理念。例如，有了人工智能算法的帮助，设计师可以根据用户的行为数据，创造出更加直观、更具吸引力的用户界面。

当然，人工智能并不是万能的。虽然它可以帮助设计师生成独特的设计，但它绝不能替代人类的创造力和直觉。不过，正如一把利器在能人之手才能发挥出威力，人工智能只有在设计师的巧妙运用下，才能展现出它的最大潜力。所以，让我们一起拥抱这个充满无限可能的新时代，让人工智能成为我们设计的得力助手吧！

- *现在主流的Ai设计工具都有哪些呢？*

目前有几种主流的人工智能设计工具。下面是一些例子：

- Canva：在图形设计领域，Canva是一款广受欢迎的工具。它利用人工智能根据用户输入来推荐设计元素和布局，让你不再为设计烦恼。

- Adobe Sensei：Adobe Sensei是设计师的天堂！这个人工智能平台提供了许多神器，比如自动图像标记、内容感知填充和字体识别等，为你的设计工作带来无限可能。

- Sketch：Sketch是设计师的得力助手。它提供了各种插件，利用人工智能自动执行重复性任务，让你专注于创造美丽的布局和设计。

- Figma：Figma是一款云端设计工具，它利用人工智能提供自动布局等功能，让你的设计工作变得更加轻松。无论何时何地，都能轻松创建出响应式设计。

- Autodesk Dreamcatcher：Autodesk Dreamcatcher是一款神奇的生成式设计工具，它利用人工智能根据用户输入的标准来生成各种设计选项，让你探索无尽的设计可能性。

以上只是冰山一角，人工智能在设计领域的运用正蓬勃发展。让我们一起期待更多创新工具和功能的问世，它们将为设计师的工作带来更多的效率和创意！

## 如何提高自己使用Stable diffusion的使用水平?

提升Stable Diffusion使用水平，你可以考虑以下几个步骤：

首先，了解Stable Diffusion的“内心世界”。在开始你的冒险之前，首先需要深入了解它的功能和使用方法。这就像是学习一项新的技能，你需要先了解它的基本原理和操作方法。例如，你需要知道如何调整模型的参数，如何使用正则化来防止过拟合，甚至如何通过扩容或剪枝模型来提高模型的精度和训练速度。

其次，理解数据和模型的内在联系。当你开始使用Stable Diffusion时，你需要清楚地了解你正在研究的现象或问题，并将其转化为数学模型。这就像是科学家通过观察自然现象，提出并验证理论的过程。你需要设计出合适的模型，并进行优化以提高它的精度和泛化能力。

然后，放手去实践并勇敢探索。通过实践，你可以不断提高自己的使用水平。你可以尝试使用不同的模型和参数进行训练和预测，然后分析结果，了解不同参数和模型对结果的影响。你也可以探索Stable Diffusion的其他功能和应用，比如进行图生成等。在这个过程中，你可能会有新的发现和收获。

此外，不要忘记学习和深化相关知识。为了更深入地了解Stable Diffusion的原理和应用，你可以学习相关的知识和技术，例如深度学习、概率图模型等。这就像是拓展你的知识视野，了解更多的技术和科学原理，这将有助于你更好地理解和使用Stable Diffusion。

最后，参与社区，分享经验并寻求帮助。你可以参与Stable Diffusion的社区活动，与其他使用者交流心得和体验，并从中获得帮助和支持。在这个过程中，你不仅可以分享你的经验，也可以从别人的经验中学习和成长。

总的来说，提高Stable Diffusion的使用水平需要不断的努力和学习。通过熟悉功能、理解数据和模型、实践和探索、学习相关知识和技术以及参与社区活动等方式，你将逐步提升你的使用水平并拓展你的应用领域。让我们一起在这个充满挑战和机遇的旅程中不断前行！



