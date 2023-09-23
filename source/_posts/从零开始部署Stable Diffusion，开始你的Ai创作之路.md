---
title: Deploying Stable Diffusion from Scratch to Start Your Ai Authoring Journey
date: 2023-05-21 08:20:32
categories:
  - Ai Drawing
tags: 
  - Stable Diffusion
  - Creative Art
  - Ai Drawing
  - Installation of Stable Diffusion
  - Stable Diffusion Model
  - Stable Diffusion in action
  - Ai Tools
  - Artistic Creation
  - Artificial Intelligence
  - Art & Design
  
description: Teach you how to deploy Stable Diffusion from scratch, and start your way to create paintings, with Chinese tutorials in the back.

cover: https://s2.loli.net/2023/07/27/cn157qIGZH9wEOm.png

---

## I. Step 1: Before deploying Stable Diffusion

There are only two types of AI painting software that are authoritative and can be used at work. One is called Midjourney (MJ for short) and the other is called [Stable Diffusion](https://stablediffusionweb.com/) (SD for short). MJ requires payment for use, while SD is open source and free, but is slightly more difficult to get started and learn, and is very expensive for computer configurations (video card, RAM).

The biggest advantage of Stable Diffusion over SD and Midjourney is that it is open source, which means that Stable Diffusion has a lot of potential and is growing rapidly.

![](https://s2.loli.net/2023/07/27/cn157qIGZH9wEOm.png)

Due to its open-source and free attributes, SD has gained a large number of active users, for which the developer community provides a large number of free, high-quality external pre-trained models ([fine-tune](https://www.finetuneus.com/)) and plug-in purposes, and constantly maintains and updates them. With the support of third-party plugins and models, SD has richer personalization features than Midjourney. After user tuning, it can generate images that are closer to the needs. Even in the field of AI video effects and AI music generation, Stable Diffusion occupies a place.

Stable Diffusion is a potential diffusion model that can generate detailed images from text descriptions. It can also be used for tasks like image restoration, image painting, text to image and image to image. In simple words, all we need to do is to give a textual description of the desired image and mention Stable Diffusion to generate a realistic image that meets your requirements!

## Step 2: Computer Configuration

The core points of the computer configuration: look at the graphics card, look at the memory, look at the hard disk, look at the CPU. one of the most important is to look at the graphics card. [Nvida Nvidia](https://zh.wikipedia.org/zh-hans/%E8%8B%B1%E4%BC%9F%E8%BE%BE) independent graphics card is preferred, the efficiency is much higher than the integrated graphics card / AMD / Intel graphics card and CPU rendering, a minimum of 10 series to start, the experience is better with the 40 series, the lowest Video memory 4G, 6G qualified, no upper limit; memory minimum 8G, 16G pass, no upper limit; hard disk available space is best to have more than 500G, solid state is best.

System requirements: support for Win10/Win11/macOS (Apple Silicon only, Intel version of the Mac can not call the Radeon graphics card) and Linux systems, Apple version of the SD-compatible plug-ins are fewer, the function is not as good as Windows and Linux computers.

![](https://s2.loli.net/2023/07/27/wprb4uiGfMKENZL.jpg)

As you can see from the graph, Nvidia's GPUs offer superior performance to anything AMD or Intel has to offer, sometimes by a wide margin. With Torch's DLL fix in place, the RTX 4090 outperforms the RTX 3090 Ti by 50 percent with xformers and 43 percent without. It takes a little over three seconds to generate each image.

## Step 3: Installation method

SD open source address: [https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki )
Currently widely used Stable Diffusion Web UI is a Python project released on the open source program sharing website [Github](https://github.com/). It differs from the usual method of installing software. It is not a software that can be used immediately after downloading and installing. It requires preparation of execution environments for different operating systems and compilation of source code.

## Step 4: Starting Stable Diffusion

! [](https://s2.loli.net/2023/07/27/dBG8qZtTrIFEHVx.jpg)

Enter the SD installation folder, double click **webui-user.bat**, load it and use Chrome to log in with the default loaded IP:*http://127.0.0.1:7860/*.

## V. Step 5: Chinese Stable Diffusion

If you need Chinese language pack, you can download the following Chinese language pack extension, the download interface URL: [https://github.com/VinsonLaro/stable-diffusion-webui-chinese](https://github.com/VinsonLaro/) stable-diffusion-webui)

***Method: Installation via WebUI extension*** 1.

1. Open stable diffusion webui and go to "**Extensions**" tab. 2.

2. Click "**Install from URL**" and note the input box under "URL for extension's git repository". 3.

3. Paste or type in the address of this Git repository [https://github.com/VinsonLaro/stable-diffusion-webui-chinese](https://github.com/VinsonLaro/stable-diffusion-webui -chinese)

4. Click the yellow button below "**Install**" to complete the installation, and then restart the WebUI (click "**Installed**" on the left of "Install from URL", and then click "**Reload UI**" at the bottom of the page with the yellow button "Apply and restart UI" to complete the reboot).

5. Click "**Settings**", left side click "**User interface**" interface, in the interface of the bottom of the "Localization (requires restart)", select "**Chinese-All**" or "**Chinese-English**".

6. Click the yellow button "**Apply settings**" at the top of the interface, and then click "**Reload UI**" on the right side to complete the localization.

## What are my feelings about using stable diffusion?

Stable Diffusion is a special kind of diffusion model that has a wide range of applications in several fields, including computer graphics, statistics, economics, and so on. Here are some of my personal thoughts and experiences in using Stable Diffusion model:

UNDERSTANDING AND IMPLEMENTATION: First of all, understanding the Stable Diffusion model requires some mathematical and physical foundation. The model is based on the Fokker-Planck equation, which involves probability theory, differential equations and other related knowledge. Therefore, it is more helpful to have some understanding of the related background. In addition, the implementation of the model also requires programming skills, which requires some knowledge of relevant programming languages and libraries.

Versatile: The Stable Diffusion model has applications in several fields. For example, in computer graphics, the model can be used to simulate the diffusion process of substances; in economics, the model can be used to simulate the fluctuation of stock prices and so on. This shows that the model has a wide range of application prospects.

Stability analysis: Stable Diffusion in this name means that its probability distribution is stable, that is, for any real numbers a and b, there is aX + bY is a stable distribution of X. Y is an independent copy of X, where Y is a stable distribution. where Y is an independent copy of X. This means that take any number of independent replicas of the stable diffusion process and the distribution remains stable. This stabilizing property makes Stable Diffusion more reliable when dealing with large amounts of data.

Handling of details: When using the Stable Diffusion model, some details need to be taken care of. For example, the initial conditions of the model, boundary conditions, time step, numerical solution method, etc. will affect the simulation results. Therefore, these parameters need to be set carefully to ensure the accuracy of the simulation results.

Limitations: although the Stable Diffusion model is able to achieve better results in many cases, there are some limitations. For example, the model assumes that the diffusion process is stable, but in some cases this assumption may not hold. In addition, the solution method of the model usually requires a large amount of computational resources, and may face the challenge of computational efficiency for large-scale problems.

FUTURE DEVELOPMENT: With the development of science and technology, the Stable Diffusion model may be further developed and improved in the future. For example, more efficient numerical solution methods can be developed, or the model can be combined with other models to adapt to more complex situations.

In conclusion, the Stable Diffusion model is a very important mathematical tool that requires certain mathematical and physical foundations in its understanding and implementation, but has a wide range of applications in several fields. In the future, with the development of science and technology, it is believed that the Stable Diffusion model will be more widely used and developed.

