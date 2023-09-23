---
title: Stable Diffusion modeling is twice the work with half the effort!
date: 2023-05-19 15:26:47
categories:
  - Ai Drawing
tags:
  - Stable Diffusion
  - Stable Diffusion model
  - Ai Drawing
  - Artistic Creation
  - Stable Diffusion in action
  - Creative Art
  - Ai Tools
  - Artistic Creation
  - Artificial Intelligence
  - Art & Design
description: Stable Diffusion model selection and model recommendation to make your work more efficient and quality.

cover: https://s2.loli.net/2023/07/27/X28Y5kEWjsAOnau.jpg

---

"Choosing the right model that produces better drawings is easier than tedious cue words."

As a matter of fact, a high-quality model can exponentially improve the quality of the outgoing image. Today, quality models have become a key factor in improving image quality. Among the many Stable Diffusion modeling communities, CivitAI (a.k.a. Station C, https://civitai.com/) has emerged as a relatively mature one, offering thousands of quality models as well as tens of thousands of well-crafted images with accompanying cue words, thus lowering the learning threshold.

Below is a brief description of some of the standout creation models from Station C, with sample application illustrations at the end of the paper.

I. Classification of Station C Models

CivitAI's models are mainly classified into four types: Checkpoint, LoRA, Textual Inversion, and Hypernetwork, which correspond to four distinctive training methods.

Checkpoint: a large model forged by Dreambooth training method, which has an exceptionally good drawing effect, but because it needs to train a brand new model, it is relatively slow and generates a large file, usually up to a few gigabytes, in safetensors or ckpt file format.

LoRA: a kind of lightweight model fine-tuning training method, it is based on the original large model for fine-tuning, in order to output people or things with specific style characteristics. It is characterized by improving the training speed while maintaining the drawing effect, and the model file is relatively small, generally in tens to more than 100 MB, which needs to be used with a large model.

Textual Inversion: a method of training models using textual cues, which can be simply understood as a set of modulation cues for creating people or things with specific stylistic features. Although its training speed is slower, the model file is small, usually tens of K, and needs to be used with a large model.
Hypernetwork: a model similar to LoRA but slightly less effective, and needs to be used with a large model.

Recommended model ranking is: Checkpoint > LoRA > Textual Inversion > Hypernetwork.

For the best mapping results, you can use the Checkpoint model with LoRA or Textual Inversion.

Bonus: There is also a VAE model, which is used to enhance the color effect of an image, making it look less monotonous and grey, while making subtle adjustments to the details of the image.

CivitAI's model filtering and searching is powerful, so you can filter the models that best suit your needs based on different categorization and sorting methods.

![](https://s2.loli.net/2023/07/27/NEsMOw2yz6YhTRp.jpg)

Once you open an individual model page, you can view model descriptions and download models.

![](https://s2.loli.net/2023/07/27/MslgPoxUcimZTWw.jpg)

## II. Model Recommendations

### -Checkpoint models

**-Lyriel-**

Model Category: Checkpoint Model

Download: [https://civitai.com/models/22922/lyriel](https://civitai.com/models/22922/lyriel)

Model Description: Competent in a variety of styles, capable of realizing top light and shadow effects and character landscape details.

Parameter recommendation: DPM++2M Karras, Clip skip 2 Sampler, Step25-35+.

![](https://s2.loli.net/2023/07/27/lL7ams3ogZeMQF2.jpg)

### -LoRA model

**-blindbox-**

Model Category: LoRA Model

Downloaded from: [https://civitai.com/models/25995/blindbox?modelVersionId=32988](https://civitai.com/models/25995/blindbox?modelVersionId= 32988)

Model Description: Can generate blindbox style model, when using it, it is recommended to select ReV Animated for the main model.

Trigger word: full body, chibi

![](https://s2.loli.net/2023/07/27/mT5V9NkJEZ1tnAl.jpg)

### -Tetual Inversion model

Model storage path: /stable-diffusion-webui/embeddings

**-SamDoesArts-**

Model Category: TETUAL INVERSION

Download Address: [https://civitai.com/models/1247/samdoesarts-embedding-1](https://civitai.com/models/1247/samdoesarts-embedding-1)

Model description: SamDoesArt painting style. Trigger word: SamDoesArt1

![](https://s2.loli.net/2023/07/27/H5c4YCXSyTBUQ2d.jpg)

Explore the infinite possibilities of AI creation
After seeing this, I believe you have deeply realized the great advantages and importance of AI models. Hurry up to pick up your creative pen and get into the sea of AI to explore the endless creative journey! As long as you make an effort to learn and master the relevant knowledge of AIGC, you can easily produce eye-catching artistic masterpieces.

Here, let's take a look at the magic keywords in the Stable Diffusion model:

- Initial seeds: Imagine that everything starts with chaos. In the world of Stable Diffusion, we need to set the initial state of diffusion, i.e. provide some "seeds" for the model.

- Time Pace: Time is the recorder of life and the conductor of the diffusion process. Each "time step" represents a small step in the process and controls the rhythm of the randomization process.

- Space: Space is the stage for diffusion. The distance traveled by the randomly diffusing particles in space in each step is the spatial pace.

- Boundary conditions: Boundaries are like ramparts that limit the range of movement of the particles. There are types such as periodic boundaries and fixed boundaries that delimit the diffusion process.

- Diffusion coefficient: Imagine that the diffusion speed of a particle through a unit area in a unit time is the diffusion coefficient, which plays a key role in the speed of the diffusion process.

- Source and sink terms: The source and sink terms are like the source and sink of the particles in the diffusion process, which can be set artificially or calculated according to the actual problem, describing the distribution of the particles in the diffusion process.

- Stabilization parameter: a small parameter, a great function! The stabilization parameter can effectively control the stability of the stochastic process, making the diffusion process more stable and preventing numerical instability.

- Gaussian Distribution: This common and amazing distribution describes the distribution of particles in a random process, and is one of the commonly used distribution functions in Stable Diffusion.

- Numerical methods: These powerful computational tools, such as Finite Difference Methods, Finite Element Methods, Spectral Methods, etc., are the key to solving the diffusion equations.

- Parallel computing: when we face large-scale diffusion problems, parallel computing is like magic, it can accelerate the calculation process, improve the efficiency of the calculation, and become a powerful tool that we must master!

These are the commonly used keywords in Stable Diffusion, they take you into the world of this model and help you understand the basic concepts, computational methods and application areas of this model. I hope you can fully enjoy the inspiration and fun brought by these keywords in your journey of exploring AI creation!




