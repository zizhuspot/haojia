---
title: Stable Diffusion How to make a cartoon version of a doll using C models
date: 2023-07-27 18:24:49
categories:
  - Ai Drawing
tags:
  - Stable Diffusion
  - Ai Drawing
  - Creative Art
  - Creative Art
  - Ai Tools
  
description: This article will show you how to use Stable Diffusion to download a model of Station C and materialize the whole process of AIGC creation by actually creating a cute cartoon doll.
cover: https://s2.loli.net/2023/07/27/rezFAto3pB7VPCm.jpg

---

## Step 1: Model Download and Loading

**Conditions**: Stable Diffusion has been successfully deployed locally.

**Required Models**: Checkpoint model (ReV Animated), Lora model (Blindbox)

- Download the LoRA model: [https://civitai.com/models/25995/blindbox?modelVersionId=32988](https://civitai.com/models/25995/blindbox? modelVersionId=32988) (to local Lora model folder /stable-diffusion-webui/models/Lora)

- Download Checkpoint model: [https://civitai.com/models/7371?modelVersionId=46846](https://civitai.com/models/7371?modelVersionId=46846) (local) Checkpoint model folder /stable-diffusion-webui/models/Stable-diffusion)

## Step 2: Setting Parameters and Prompt Words

Besides manually inputting prompt words and setting parameters, there is an easier way: directly copy parameters from CivitiAI artwork to WebUI with one click, and then adjust them.

![](https://s2.loli.net/2023/07/27/py2MabrNl37KRSV.jpg)

![](https://s2.loli.net/2023/07/27/WXaoYDLrkqfedNO.jpg)

***Prompts and Parameter Settings:***

**Pompt** : (masterpiece), (best quality), (ultra-detailed), (full body:1.2), (simple background, white background:1.3), chibi, simple body, melting heart, purple leaves, purple hat, vivid color

**Negative Prompt**: (worst quality, low quality:1.4), lowres, bad anatomy, bad hands, text, error, missing fingers, extra digit, fewer digits, cropped, worst quality, low quality:1.2), (simple background, white background:1.3), chibi, simple body, melting heart, purple leaves, purple hat, vivid color cropped, worst quality, low quality, normal quality, jpeg artifacts, signature, watermark, username, blurry

*Steps: 20, Sampler: DPM++ SDE Karras, CFG scale: 7.5, Size: 512x768*, Size: 512x768*, Sampler: DPM++ SDE Karras, CFG scale: 7.5, Size: 512x768

## Step 3: Setting up ControlNet to customize the bobblehead's image

In this example, we want to make a 3D bobble head doll from a flat cartoon, so we need to use the lineart and depth model of [ControlNet](https://stablediffusionweb.com/ControlNet) to build the bobble head's outline, and then overlay the blind box model to customize the bobble head doll. image.

The model is then superimposed on the blind box model to customize the figurine. [](https://s2.loli.net/2023/07/27/rezFAto3pB7VPCm.jpg)

## Summary:

By making a cute cartoon doll with your own hands, I believe you have gained an intuitive understanding of how to work with models. Only by trying your hand can you really grasp how the whole workflow is realized. I hope you all can learn more about AI art creation from this!

Let's talk about some of the application areas of AI drawing!
Data visualization: AI drawing can easily present a large amount of data in the form of charts and graphs, making the data more visible and easy to understand. For example, we can use AI drawing to generate line graphs, bar charts, scatter plots, etc., to help us better understand the trend of the data, distribution and other information.

AI mapping can also generate various types of images, including natural landscapes, portraits, artworks, and more. By training the model, AI can learn and mimic various painting styles, thus generating extremely artistic and beautiful images oh!

In addition, AI drawing also shines in the design and creative fields. It can be used to draw graphic design, illustrations, logos, posters, etc. According to the user's needs and input parameters, it generates a design pattern that meets the requirements and adds to your creative endeavors!

Finally, AI Drawing is also a powerful auxiliary drawing tool. It can help artists, designers, etc. to quickly generate sketches, line drawings and other preliminary ideas, thus improving creative efficiency. In short, AI drawing can work its magic in many fields, helping people to better express and present information, and improve creative efficiency and creativity!

## * Can AI and design work together? *

Yes, AI can indeed be used for design, and it's already being used in a variety of fields. Imagine everything from logos to web layouts to fashion design, the potential of AI is truly endless! It acts like a tireless assistant, automating repetitive tasks and helping designers easily analyze data to find hidden patterns and insights.

Not only that, but AI can also bring new design ideas to designers. For example, with the help of AI algorithms, designers can create more intuitive and attractive user interfaces based on user behavioral data.

Of course, AI is not a panacea. While it can help designers generate unique designs, it can never replace human creativity and intuition. However, just as a sharp weapon can only be powerful in the hands of a capable person, AI can only show its maximum potential when skillfully utilized by designers. So, let's embrace this new era full of infinite possibilities and let AI become our right-hand man in design!

## * What are the mainstream Ai design tools now? *

There are several mainstream AI design tools available. Here are some examples:

- Canva: Canva is a popular tool in the graphic design field. It utilizes artificial intelligence to recommend design elements and layouts based on user input, taking the hassle out of designing.

- Adobe Sensei: Adobe Sensei is a designer's paradise! This AI platform offers a number of wonders such as automatic image markup, content-aware fills, and font recognition that open up endless possibilities for your design work.

- Sketch: Sketch is a designer's right-hand man. It offers a variety of plugins that utilize artificial intelligence to automate repetitive tasks, allowing you to focus on creating beautiful layouts and designs.

- Figma: Figma is a cloud-based design tool that utilizes artificial intelligence to provide automated layouts and other features to make your design work easier. Easily create responsive designs whenever and wherever you want.

- Autodesk Dreamcatcher: Autodesk Dreamcatcher is an amazing generative design tool that utilizes artificial intelligence to generate a variety of design options based on user-entered criteria, allowing you to explore endless design possibilities.

The above is just the tip of the iceberg; the use of AI in design is booming. Let's look forward to more innovative tools and features that will bring more efficiency and creativity to designers' work!

## How can I improve my use of Stable diffusion?

There are several steps you can take to improve your use of Stable Diffusion:

First, get to know the "inner workings" of Stable Diffusion. Before you start your adventure, you need to have a deep understanding of what it does and how to use it. It's like learning a new skill, you need to understand the basics and how it works. For example, you need to know how to tune the parameters of the model, how to use regularization to prevent overfitting, and even how to improve the accuracy and training speed of the model by expanding or pruning it.

Next, understand the intrinsic connection between the data and the model. When you start using Stable Diffusion, you need to have a clear understanding of the phenomenon or problem you are studying and translate it into a mathematical model. This is like the process by which scientists propose and validate theories by observing natural phenomena. You need to design a suitable model and optimize it to improve its accuracy and generalization.

Then, let go of practice and explore bravely. By practicing, you can keep improving your usage. You can try to use different models and parameters for training and prediction, and then analyze the results to understand how different parameters and models affect the results. You can also explore other features and applications of Stable Diffusion, such as performing graph generation. In the process, you may make new discoveries and gains.

In addition, don't forget to learn and deepen your knowledge. In order to understand the principles and applications of Stable Diffusion more deeply, you can learn related knowledge and techniques, such as deep learning, probabilistic graph models, and so on. This is like expanding your knowledge horizons to learn more about technical and scientific principles, which will help you better understand and use Stable Diffusion.

Finally, get involved in the community, share your experiences and ask for help. You can participate in Stable Diffusion's community to share your tips and experiences with other users and get help and support from them. In the process, you can not only share your experience, but also learn and grow from others' experience.

Overall, improving your use of Stable Diffusion requires continuous effort and learning. By familiarizing yourself with the features, understanding the data and models, practicing and exploring, learning related knowledge and techniques, and participating in community activities, you will gradually improve your usage and expand your application areas. Let's move forward together on this journey full of challenges and opportunities!



