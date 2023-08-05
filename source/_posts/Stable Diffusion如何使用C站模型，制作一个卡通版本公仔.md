---
title: Stable Diffusion如何使用C站模型，制作一个卡通版本公仔
date: 2023-07-27 18:24:49
categories:
  - Ai绘图
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
  
description: 本文介绍了使用Stable Diffusion下载C站模型，实战创作一个卡通公仔，对于AIGC整个创作流程更具体化
  。
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

## 设置ControlNet，定制公仔专属形象

在这个实例中，我们要把一个平面卡通形象制作成一个 3D 公仔形象，因此需要通过[ControlNet](https://stablediffusionweb.com/ControlNet)的 lineart 和 depth 模型，构建公仔轮廓，再叠加盲盒模型定制出专属公仔形象。

![](https://s2.loli.net/2023/07/27/rezFAto3pB7VPCm.jpg)

## 总结：

通过这个制作卡通公仔的形象，相信大家对于如何使用模型已经有了一个基本的了解，最好自己动手试一试，才知道整个工作流程是如何实现的，最后祝大家学到更多的Ai艺术创作知识。


